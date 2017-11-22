#Smart Image Resizer

Resizes images, intelligently sharpens, crops based on width:height ratios, color fills
transparent GIFs and PNGs, and caches variations for optimal performance

Created by: Joe Lencioni ([http://shiftingpixel.com](http://shiftingpixel.com))
Date: August 6, 2008
Based on: http://veryraw.com/history/2005/03/image-resizing-with-php/

Updated By: Nate Nolting ([naten@paulbunyan.net](mailto:naten@paulbunyan.net))

##LICENSE

> "I love to hear when my work is being used, so if you decide to use this, feel encouraged
> to send me an email. Smart Image Resizer is released under a Creative Commons
> Attribution-Share Alike 3.0 United States license
> ([http://creativecommons.org/licenses/by-sa/3.0/us/](http://creativecommons.org/licenses/by-sa/3.0/us/)). All I ask is that you include a link
> back to Shifting Pixel (either this page or shiftingpixel.com), but don't worry about
> including a big link on each page if you don't want to; one will do just nicely. Feel
> free to contact me to discuss any specifics ([joe@shiftingpixel.com](mailto:joe@shiftingpixel.com))."
-- Joe Lencioni

##REQUIREMENTS

* PHP
* GD

##INSTALL VIA BOWER

```
    bower install image.php#1.4.4 -S
```

## PARAMETERS

Parameters need to be passed in through the URL's query string:

| Param  | Description |
|---|---|
|  image | absolute path of local image starting with "/" (e.g. /images/toast.jpg) |
|  width | maximum width of final image in pixels (e.g. 700) |
|  height | maximum height of final image in pixels (e.g. 700) |
|  color | (optional) background hex color for filling transparent PNGs (e.g. 900 or 16a942) |
|  cropratio | (optional) ratio of width to height to crop final image (e.g. 1:1 or 3:2) |
|  nocache | (optional) does not read image from the cache |
|  quality | (optional, 0-100, default: 90) quality of output image |

##EXAMPLES

Resizing a JPEG:

```
<img src="/image.php/image-name.jpg?width=100&amp;height=100&amp;image=/path/to/image.jpg" alt="Don't forget your alt text" />
```

Resizing and cropping a JPEG into a square:

```
<img src="/image.php/image-name.jpg?width=100&amp;height=100&amp;cropratio=1:1&amp;image=/path/to/image.jpg" alt="Don't forget your alt text" />
```

Matting a PNG with #990000:
```
<img src="/image.php/image-name.png?color=900&amp;image=/path/to/image.png" alt="Don't forget your alt text" />
```
