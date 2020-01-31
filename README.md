# Music Forecaster

This notebook is made to introduce time series analysis in a fun way! We train an AI to make its own music based on a music file.

This notebook requires
<br>tensorflow
<br>scipy
<br>matplotlib
<br>numpy
<br>pandas

The main sections are:
1. Load Wav File  - we load a midi music in WAV format
* Split Wav Data into Distinct Elements - we find the "beats" of the music and split by beats
* Find Notes In each Element Using Fourier Transform - using Fourier transformation, we find the frequencies associated with each beat
* Convert into "Music Sheet" - we convert the wav form where the y-axis is amplitude and x-axis is time into a "music sheet" form where the y-axis is the frequency and the x-axis is time. In summary, the transformation is: wav form 1 -> fourier transform -> music sheet -> wav form 2. 
* Prepare for Training Model - we transform the "music sheets" into a form for our deep learning model. We define a deep learning model called LSTM which will be trained to predict the next notes based on past notes
* Training Model - here is where we train the model on the transformed dataset
* Predict - here is where we use the trained model to predict the last 20% of the music based on the first 80% of the music
* Convert Notes from Frequencies to Waves - here is where we transform the predictions from "music sheet" into WAV format

Input: canon.wav

Outputs:
1. 
