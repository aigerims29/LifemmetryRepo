---
layout: post
title: "How to make Gigapixel images"
date: 2019-01-11
author: "Joan Cano"
categories: [photography]
tags: [photography]
---

The curiosity of this week has been how to make Gigapixel images..

In the last post we wrote, we talked about how to take 360º photos. Making Gigapixel images is not much different.

The first step is to take the photos, but how? If you remember, to make the images for the 360º, we must have a % of overlap between images, in addition to covering the whole sphere.

The process to perform the gigapixel is similar. If we have a camera with a 14-70 mm lens, we should take the photos with the maximum focal length, in this case 70 mm. That is to say, we will take ALL the images with the greatest possible focal length, or we will decide the *f* according to the level of detail that we want to obtain.

In this moment in which we already know how to shoot the photos, we have two ways available to help get our images without any gap in the final image:

- The first option is to shoot manually, so it is a matter of making a puzzle of our final image, for example by choosing two points that act as the beginning and the end (both longitudinally and latitudinally).
- Buy a robotic arm that shoots and places the camera for us.

The next step would be to build the gigapixel, so we could follow the same steps that were used in the previous post [how to make 360 ​​photos](https://lifemmetry.github.io/LifemmetryR/vr/2019/01/02/02/ 360-photos.html), but instead of choosing a cylindrical projection we would choose the planar one.

The last step would be to share the image. As it is a very wide lateral image we will need a viewer that allows us to move through it, and fluidly.

Many softwares have been tried.. MANY! most of them being discontinued. I recommend 2:

+ GDAL + Leaflet (Open Source option)
+ Panotour (commercial)

To use GDAL and Leaflet in Linux, we will install GDAL:

`$ sudo apt install gdal-bin`

Once we have GDAL installed, we must execute the command in the terminal:

`$ gdal2tiles -p raster ourImage.jpg ourDestinyFolder`

And we will have our viewer!

For GDAL to create an html with Leaflet and not OL automatically, include *-l*:

`gdal2tiles.py -l -p raster ourImage.jpg ourDestinyFolder`

I still do not understand why, but when I have processed the *png* and *tiff* formats, the result has unexpectedly generated tiles with chromatic changes. So I recommend processing this type of images without any type of coordinate system in *jpg* format!

PS: here one of the viewers made:
+ [From mesh] (http://files.tecnitop.com/usuarios/joan/wordpress/tourMP.html)
+ [Gigapixel of the Serra de Bèrnia] (https://joancano.github.io/joancano.io/gigaBernia/gigaBernia.html)
