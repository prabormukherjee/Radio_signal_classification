# Radio_signal_classification

Here using a dataset I classified Radio signal coming from space. The dataset has a lot of features. I just used some simple CNN technique. Although the performance can be imporved b hyperparameter tuining. I just showed how to make this kind of model.
<br>
The dataset is provided by <a href='https://www.seti.org/'>SETI</a>.What they do is they use their Allen telescope array & wide range of antennas to scan the night sky for very faint radio signals, from the outer space. What we will do is we’ll treat these 2-D Spectrograms as images and put them in our image classifier to classify these faint radio signals into one of the four categories.To give you a bit more context, at the SETI institute they use the Allen telescope array situated in northern California to scan the sky at various radio frequencies to observe the star system with known exoplanets. The goal is to search for faint but persistent signals.
<br>
The current signal detection system is programmed for only particular kinds of signals such as narrow-band carrier waves however, the detection system sometimes triggers the signals that are not narrow-band signals with some unknown efficiency and are also not explicitly known frequency interference. So there seem to be various categories of these kinds of events that have been observed in the recent past so our goal for the next few minutes is to build an image classification model to classify these signals accurately in real-time so this may allow the signal detection system to make better observational decisions and thereby increasing the efficiency of the night scans, allowing for explicit detection of signal types. So the original signals were not 2-D spectrograms but were time-series data collected and downloaded by Seti. We’re going to work with 2-D spectrograms which were created by transforming the input time-series data. So we’re going to use the spectrograms as images to train or classification model. By the end of this blog, you will learn to build & train a CNN by scratch to classify these radio signals from space.
<br>
How can images be stored in a CSV file ? The spectrograph images were converted into their raw pixel intensity values and were normalized so the values lie between 0 and 1. They are then converted into an array by stretching them. Therefore each row of the CSV file corresponds to a single image. Each Row Corresponds to an image. The label were found to be one hot encoded in to a vector of 1,4(no. of classes). 
<ul>
  <li>1,0,0,0 is squiggle</li>
  <li>0,1,0,0 is Narrow-band signal</li>
  <li>0,0,1,0 is Noise</li>
  <li>0,0,0,1 is Narrow-band-drd signal</li>
</ul>
The dataset is very large. I added as much as possible but `training/images` is misssing due to its huge size.I added all other part of the data except this one. The total dataset can be found <a href='https://drive.google.com/open?id=13L9jFnThO7lxBsToQkQZ9TUYazIK9mWR'>here</a>, in the drive link. I provided the source code.
