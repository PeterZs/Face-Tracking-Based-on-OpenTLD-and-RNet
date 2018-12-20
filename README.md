### Face-Tracking-Based-on-OpenTLD-and-RNet

I optimized OpenTLD making it run faster and better for face tracking.

This version of TLD below is faster and more stable than that in OpenCV. I delete some funtions to make it run faster. What is more, use RNet to judge the face that TLD produced to avoid TLD tracking a wrong target. In order to get a stable bounding box, I fix the width and height that MTCNN provides when initialising. Running speeds on my PC(Intel® Xeon(R) CPU E5-2673 v3 @ 2.40GHz × 48) are about 30ms(MTCNN, ncnn), 30ms(TLD initial), 10ms(TLD tracking). Besides, MTCNN can be replaced by PCN or any other face detection algorithms.

中文地址：https://blog.csdn.net/renhanchi/article/details/85089265

### Installing

OpenCV 2.4.X is required!

Reset your ncnn path in CMakeLists.txt.

```shell
mkdir build
cd build
cmake ..
make
cd ../bin
./demo
```

### Examples

![image](https://github.com/HandsomeHans/Face-Tracking-Based-on-OpenTLD-and-RNet/blob/master/example/saved_1.gif)

![image](https://github.com/HandsomeHans/Face-Tracking-Based-on-OpenTLD-and-RNet/blob/master/example/saved.gif)

### References

https://github.com/CongWeilin/mtcnn-caffe

https://github.com/alantrrs/OpenTLD
