clear all;
close all;
clc;

image = imread('cricket ball.jpg');


red = image(:,:,1);
green = image(:,:,2);
blue = image(:,:,3);

figure(1)
subplot(2,2,1);imshow(image); title('Original');
subplot(2,2,2);imshow(red);title('Red');
subplot(2,2,3);imshow(green);title('Green');
subplot(2,2,4);imshow(blue);title('Blue');

figure(2)
bw = imbinarize(blue,0.30);
subplot(2,2,1);imshow(bw);title('Blue');

fill = imfill(bw,'holes');
subplot(2,2,2);imshow(fill);title('Holes filled');


clear = imclearborder(fill);
subplot(2,2,3);imshow(clear);title('Blobs on border');


se = strel('disk',7);
open = imopen(fill,se);
subplot(2,2,4);imshow(open);title('Remove small blobs');


diameter = regionprops(open,'MajorAxisLength')


figure(3)
imshow(image)
d = imdistline;








