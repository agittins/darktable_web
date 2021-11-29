# Darktable_web

Status: Not even a minimum viable product, yet. Does nothing.

This is (to be) a simple Django app for browsing your darktable library using
a web browser. Start this on your machine that hosts darktable, point it
at your library and you can browse your library from a local web
browser, or if you trust your local network, on a tablet etc.

Often when I get home from a shoot I want to browse through my images,
but I don't necessarily want to sit at the computer to do it, or maybe I
want to show them off to my partner as she politely nods. This app is to
allow me to do that on a tablet or phone, once the new images have been
imported into darktable and the thumbnail cache is generated.


Caveats:

- No image processing is done AT ALL. The web server assumes that it
  will be able to find cached thumbnails already generated, and will
  serve those.
    - Use `darktable-generate-cache --min-mip 0 --max-mip 5` say, to
      pre-generate the images that this app will serve.
- This is for browsing only, not editing images. 
- One day I plan to add support for rating and tagging images to make it
  easy to do the initial _Culling From The Couch_(tm).

