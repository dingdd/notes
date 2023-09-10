1#yHbj53

from scipy.io.wavfile import read
(fs, x) = read('pianoS.wav')
(fss, xx) = read('pianoMono.wav')

import numpy as np

np.max(x)
np.min(x)

https://spritely.institute/static/papers/scheme-primer.html

(lambda (x) (* x 2))           ; procedure (we'll come back to this)
'(lambda (x) (* x 2))          ; a list of lists, symbols, and numbers


Finally, Scheme's procedures can do something else interesting: they can return multiple values using… values! As a particularly silly example, perhaps we would like to compare what it's like to both add and multiply two numbers:

REPL> (define (add-and-multiply x y)
        (values (+ x y)
                (* x y)))
REPL> (add-and-multiply 2 8)
; => 10
; => 16
REPL> (define-values (added multiplied)
        (add-and-multiply 3 10))
REPL> added
; => 13
REPL> multiplied
; => 30
As you can see, we can capture said values with define-values, as shown above. (let-values and call-with-values can also be used, but that's enough new syntax for this section!)


So, we could write a silly function that excitedly reports on whether or not an object is a string or not:

REPL> (define (string-enthusiast obj)
        (if (string? obj)
            "Oh my gosh you gave me A STRING!!!"
            "That WASN'T A STRING AT ALL!! MORE STRINGS PLEASE!"))
REPL> (string-enthusiast "carrot")
; => "Oh my gosh you gave me A STRING!!!"
REPL> (string-enthusiast 529)
; => "That WASN'T A STRING AT ALL!! MORE STRINGS PLEASE!"
As we can see, unlike in some other popular languages, if also returns the value of evaluating whichever branch is chosen based on <TEST>.

What is the return of else branch when condition is false


map performs some extra work by building up a list of results every time. But what if we wanted to simply display our love of some food to the screen using display and did not care about operating on the data any further? We could use for-each, which has the same structure as map but does not build a result:

REPL> (for-each (lambda (str)
                  (display
                   (string-append "I just love "
                                  (string-upcase str)
                                  "!!!\n")))
                '("ice cream" "fudge" "cookies"))
; prints:
;   I just love ICE CREAM!!!
;   I just love FUDGE!!!
;   I just love COOKIES!!!


/etc/network/interfaces 
/etc/network/interfaces.d/eth0
sudo /etc/init.d/networking restart

num=`grep VERSION_BUILD version.h  | sed 's/\r//g' | sed 's/[[:blank:]]\+/ /g' |cut -d ' ' -f 3`; next=`expr $num + 1`; sed -i "s/$num/$next/g" version.h

play -n -c1 synth sin %-12 sin %-9 sin %-5 sin %-2 fade q 0.1 1 0.1
plays a synthesised 'A minor seventh' chord with a pipe-organ sound,

C++ type_trait是干什么用的？

audacity Signal读值为什么会是负的呢？

Audacity pitch tempo speed, sox ?

服务器启动，slave端什么时候下载下来的？

Nyquist Shannon 采样定理

set up a git server

change pitch tempo speed

QT lingusist 怎么用的?

Canny

findContours

MinBoundingRect

-platform linuxfb

pointPolygonTest

RotatedRect

isContinuous

minEnclosingTriangle

approxPolyDP

https://docs.opencv.org/4.x/dc/d48/tutorial_point_polygon_test.html

为什么通过python 启动和直接启动有区别 一个停在No Image 一个是摄像头
 为什么需要sudo来启wmcam_slave_v2
 Working Thread processDetectLFI时为什么需要QMutexLocker
 FloatingForm是干什么用的，用在哪里
 Forminformation.ui的上标0.001是怎么打出来的
 
 opencv的Mat不是多维的么，为什么还可以rowRange, colRange
  A.row(i) += A.row(j)*alpha;
  A.row(i) = A.row(j) + 0; Mat怎么可以与数字相加
  https://docs.opencv.org/3.4/d3/d63/classcv_1_1Mat.html#a4b22e1c23af7a7f2eef8fa478cfa7434
  
  
  ./modules/core/src/matrix_expressions.cpp中的makeExpr定义在哪里？，我找不到啊
  
  
  windows下opencv的环境
  
  F:\opencv-4.5.3\build\binopencv_test_imgproc.exe 无法找到入口
  
  
  An array can be indexed by a tuple of nonnegative integers, by booleans, by another array, or by integers.
  https://numpy.org/doc/stable/user/absolute_beginners.html
  
  
  For 3-D or higher dimensional arrays, the term tensor is also commonly used.为什么3维及以上的称作tensor
  
  
In [3]: a = np.zeros(4)
		print(a)
		b = np.zeros((2,3), dtype = np.float32)
		print(b)
		c = np.zeros((2,2), dtype = [('x', 'i4'), ('y', 'f4')])
		print(c)
Out[3]: [0. 0. 0. 0.]
		[[0. 0. 0.]
		 [0. 0. 0.]]
		[[(0, 0.) (0, 0.)]
		 [(0, 0.) (0, 0.)]]
————————————————
版权声明：本文为CSDN博主「n南x星」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/weixin_50517509/article/details/125595673

dtype是什么类型的？


Just like in other Python container objects, the contents of an array can be accessed and modified by indexing or slicing the array. Unlike the typical container objects, different arrays can share the same data, so changes made on one array might be visible in another.?

1 2 3
4 5 6

opencv fillPoly函数的Point参数为什么是指向指针的指针

https://homepages.inf.ed.ac.uk/rbf/CVonline/LOCAL_COPIES/MANDUCHI1/Bilateral_Filtering.html     Bilateral Filtering


https://docs.opencv.org/4.x/d3/dbe/tutorial_opening_closing_hats.html    Top Hat      Black Hat


opencv Mat_ template<typename _Tp> class Mat_ : public Mat 有什么用？

MatExpr的alpha和beta是什么意思

Mat.convertTo saturate_cast   


Mat 为什么可以用多维数组来初始化，

Distance transform real-valued images


-lopencv_wechat_qrcode
-lopencv_barcode



barCode 定位


batcode.cpp 132 -------   std::vector<std::string> qr_codes = qr_detector->detectAndDecode(image, qr_points);


F:\wmcamv2_src_2023.01.03\wmcamv2\modules\algorithms\util.cpp:238

F:\wmcamv2_src_2023.01.03\wmcamv2\apps\wmcam_slave_v2\workthread.cpp:78

/usr/local/include/opencv4/opencv2/wechat_qrcode.hpp:36

cv::wechat_qrcode::WeChatQRCode
std::vector<cv::Mat> qr_points;
std::vector<std::string> qr_codes = qr_detector->detectAndDecode(image, qr_points);

返回的4个点在Mat[0][0] mat[0][1] mat[1][0] mat[1][1]上?


为什么一次二维码开始会检测4次
----------------------------------0-----------------------------------------
decode-1: 61: https://logistics-mrd.jd.com/cmail?deliveryId=JDX002089769870
----------------------------------1-----------------------------------------
decode-1: 61: https://logistics-mrd.jd.com/cmail?deliveryId=JDX002089769870
----------------------------------1-----------------------------------------
decode-1: 61: https://logistics-mrd.jd.com/cmail?deliveryId=JDX002089769870


样机是如何采样的15帧每秒

为什么会连续收到IDLE信号？
(((((((((((((((((((((((((0))))))))))))))))))))))
(((((((((((((((((((((((((0))))))))))))))))))))))
(((((((((((((((((((((((((0))))))))))))))))))))))
(((((((((((((((((((((((((0))))))))))))))))))))))
(((((((((((((((((((((((((0))))))))))))))))))))))
(((((((((((((((((((((((((0))))))))))))))))))))))
(((((((((((((((((((((((((0))))))))))))))))))))))


-------------------------Time elapsed: 128 ms
decode-1: 61: https://logistics-mrd.jd.com/cmail?deliveryId=JDX002089769870
----------------------------------1-----------------------------------------
-------------------------Time elapsed: 84 ms
decode-1: 61: https://logistics-mrd.jd.com/cmail?deliveryId=JDX002089769870
----------------------------------1-----------------------------------------
-------------------------Time elapsed: 98 ms
decode-1: 61: https://logistics-mrd.jd.com/cmail?deliveryId=JDX002089769870


