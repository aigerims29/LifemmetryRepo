---
layout: post
title: How to make pannellum viewers
date:   2019-01-04 13:50:39
categories: VR
---

Making panoramas with Panellum.

The code are 3 files:
- panellum.html
- panellum.js
- panellum.css

This is the code of the html:


```
<!DOCTYPE HTML>
<!-- Pannellum 2.4.0, https://github.com/mpetroff/pannellum -->
<html>
<head>
  <meta charset=utf-8>
  <meta name=viewport content="width=device-width, initial-scale=1.0">

   <link rel="stylesheet" href="pannellum.css">
   <script type="text/javascript" src="pannellum.js"></script>

  <title>Pannellum</title>
  <style>
   #panorama {
       width: 700px;
       height: 350px;
   }
   </style>

   <body>
   <div id="panorama"></div>
					<script>
						pannellum.viewer('panorama', {
						"type": "equirectangular",
						"title":"Ponoig",
						"author":"Joan Cano",
						"panorama": "ponoig.jpg",
						//"autoLoad": true,
						"compass": true
						});
					</script>
  </body>
  </html>

```

And is the in the folder `static`, which is the same in the first folders and the folders inside `_site`.


[DEMO](../static/panoponoig.html)
