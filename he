
#include <string>
#include <iomanip>
#include <sstream>
 
#include <opencv2/imgproc/imgproc.hpp>
#include <opencv2/core/core.hpp>
#include <opencv2/highgui/highgui.hpp>
#include <iostream>

using namespace cv;
using namespace std;

 
int main(int argc, char *argv[]){
    Mat frame,bh,gh,rh,img_hist_equalized,img_histequalized;
    frame = cvLoadImage( argv[1] );
    vector<Mat> ch;
        Mat output (frame.size(),frame.type());
        vector<Mat> rgb;
        //vector<Mat> hsv;
        //vector<Mat> ycrcb;
        //cvtColor(frame,output,CV_RGB2YCrCb);
        // split(frame, rgb);
        split(frame, rgb);
 	equalizeHist( rgb[0], bh );
 	equalizeHist( rgb[1], gh );
 	equalizeHist( rgb[2], rh );   
        namedWindow( "k", WINDOW_AUTOSIZE );
        
        ch.push_back(bh);
    	ch.push_back(gh);
   	ch.push_back(rh);

        merge(ch,img_hist_equalized); 
 	imshow("k",img_hist_equalized);

 
    
    waitKey(0);
}
