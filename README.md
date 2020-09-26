# Image_processing
## Problem 1. Hybrid Images
In this problem I created hybrid images as described in [1]. </br>
Take two images, A and B, that you’ll want to have blend from one to the other. Try to make the objects in the two images occupy more or less the same region. Construct a hybrid image from A (to be seen close-up) and B (to be seen far away) as follows:</br>
out = blur(B) + (A-blur(A)) </br>
### Gaussian filter
You can use gaussian function to low-pass filters the image. By increasing sigma and kernel size the output will become smoother.</br>
![Gaussian filter]()
### Box filter
Box blur is also known as box linear filter. Box blurs are frequently used to approximate Gaussian blur. Here is the result of applying box blur with kernel size = 3 on both images.</br>
![Box filter]()
### Hybrid images
Gaussian filter:
The hybrid image when we want to see the cat up close is shown in the first row with different sigma value, and the hybrid for seeing the monkey up close is presented in the second row.</br>
![Hybrid images]()
As we increase sigma, we pass higher frequencies in our low pass filter. This means the image corresponding to low pass frequency (far image) can be seen more clearly in the front and the other image corresponding to higher frequency (1-low pass) will have less frequency therefore is less visible in the front.</br>
## Problem 2. De-hybridizing
By applying a low pass filter on the hybrid image we can extract low frequencies that correspond to the far image. Then we will subtract them from hybrid image to get the high frequencies related to einstein image. </br>
![De-hybrid images]()

References
[1] Aude Oliva, Antonio Torralba, and Philippe G Schyns. Hybrid images. ACM Transactions
on Graphics (TOG), 2006.
