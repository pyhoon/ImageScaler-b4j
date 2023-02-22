# ImageScaler-b4j
A B4J wrapper from ImgScalr (https://github.com/rkalla/imgscalr)

**Current version:** 1.0

# Introduction: #

I don't know if there is any library exist to resize image in B4J non-UI app.
I thought such library will be useful to process images for web server in building REST API for e-commerce or e-learning web apps.
I found [an example on web](https://www.baeldung.com/java-resize-image) and chose the third method, from an old project call [ImgScalr](https://github.com/rkalla/imgscalr).
I done some experiments and manage to get it work in B4J using Inline Java.
Then I tried to compile the project as a library. boop! Done. It is so easy and I have my .jar and .xml files ready to use.

# Supported file types: #
JPG

JPEG

PNG

BMP

WBMP

Note: GIF is not supported

# Usage: #
```vb
Sub ResizeImages
    Private img As ImageScaler
    img.Initialize
    img.ResizeImage(File.DirApp, File.DirApp, "Sonic.jpg", 200, 200, "AUTOMATIC")
    img.ResizeImage(File.DirApp, File.DirApp, "Puss.png", 300, 300, "FIT_TO_WIDTH")
    img.ResizeImage(File.DirApp, File.DirApp, "Logo.bmp", 150, 150, "FIT_TO_HEIGHT")
End Sub
```

## Additional Jars (Dependencies): ##
[imgscalr-lib-4.2.jar](https://mvnrepository.com/artifact/org.imgscalr/imgscalr-lib/4.2)
