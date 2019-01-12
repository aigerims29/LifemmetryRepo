---
layout: post
title: How to make pannellum viewers
date:   2019-01-04 13:50:39
categories: photography
---

We need to have 4 files. Among them are the JS and CSS that must be downloaded from [the website](https://pannellum.org/). The html we have to build us and of course, the image too;).

- panellum.html
- panellum.js
- panellum.css
- image

<iframe width="800" height="500" src="../../../../static/panos/panellum.html" frameborder="0" allowfullscreen></iframe>

And this would be the html code, look to the container 'panorama':

```
<!DOCTYPE html>
<html lang="en">

<head>

    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="author" content="joan" >

    <title>Guate</title>

    <link rel="stylesheet" href="pannellum.css">

     <style>
     body, html{
       width: 100%;
       height: 100%;
       margin: 0;
     }
    #panorama {
        width: 100%;
        height: 100%;
    }
    </style>

    <script type="text/javascript" src="pannellum.js"></script>

</head>

<body>

  <div id="panorama"></div>
		<script>
		  pannellum.viewer('panorama', {
			"type": "equirectangular",
			"title":"Escuelita",
			"author":"Joan Cano",
      "panorama": "pano2.jpg",
			"compass": true
			});
		</script>

</body>

</html>
```
