# Realtime Arbitrary Webcam Style Transfer

![Demo of webcam arbitrary style transfer](https://raw.githubusercontent.com/heaversm/arbitrary-webcam-style-transfer/master/demo.gif)

### Rationale

Normally, creating a style image for style transfer requires training a model for numerous hours on a computer with a strong GPU at the cost of cloud computing time and significant energy use for processer usage, not to mention the hassle of setting up all the necessary library dependencies for training. 

With arbitrary style transfer, style images can be selected without the training and styles applied to the content image in real-time. This demo takes the user's webcam image, applies the given style, and renders it out to an html canvas. 

### Usage

Simply spin up a local dev server (`python -m http.server` if you have python3 installed, or `python -m SimpleHttpServer` for python2), open your browser to the selected directory (http://localhost:8000, by default with python), and allow access to your webcam. A web server is required in order to gain permissions to the webcam.

Click on the select file button and load an image to replace the pre-existing style image, then wait for the webcam to render you in the style of that image.

**Note**: Real-time style transfer is processor intensive and runs slowly on all but the most powerful machines. You can expect significant lag on even a fairly modern laptop unless it has a good GPU. To improve results, keep your images small.



### Credits

Uses [Reiichiro Nakano](https://github.com/reiinakano/arbitrary-image-stylization-tfjs)'s Tensorflow.js port of Ghiasi et al.'s [fast arbitrary style transfer model](https://github.com/tensorflow/magenta/tree/master/magenta/models/arbitrary_image_stylization) within [Magenta](https://magenta.tensorflow.org/) for [Tensorflow.js](https://www.tensorflow.org/js).

Discovered as part of my participation in [Romie Littrell's](https://www.linkedin.com/in/romie-littrell/) installation for "[The End of You](https://endofyou.io/)" at [Gray Area](https://grayarea.org/) San Francisco

