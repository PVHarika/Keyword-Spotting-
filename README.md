# Keyword Spotting
In this project we have used google speech command version 2 
It contains 35 different word recordings of common commands (.wav format). 
The commands are: yes, no, up,down, left, right, on, off, stop, go, zero, one, two, three, four,five, six, seven, eight, nine, bed, bird, cat, dog, happy, house, marvin, sheila, tree, wow, backward, forward, follow, learn, visual.
# Distribution of Audio files
Dataset has divided into three segments:
● Training set - 80.2% - 84843 audio files. ● Testing set - 10.4% - 9981 audio files. ● Validation set - 9.4% - 11005 audio files.

![Screenshot 2024-02-17 113237](https://github.com/PVHarika/Keyword-Spotting-/assets/147228955/45643d80-69d1-45b2-891d-56b9404d939d)
# Data Pre-processing 
We observed that most of the files have a shape of 16000, 
it means 16000 samples for 1 sec. 
But few have less number of samples andfew have more than 16000.

![Screenshot 2024-02-17 113937](https://github.com/PVHarika/Keyword-Spotting-/assets/147228955/1249e2f3-0921-4fc2-8d25-a5b81a0afdd8)

To normalize the data, the files with less number of samples, we will do padding for that, and for more number of samples,
we will do trimming for that.

![Screenshot 2024-02-17 114135](https://github.com/PVHarika/Keyword-Spotting-/assets/147228955/b8096c40-7d25-4440-9236-326dd8815632)

# Feature extraction 
● We extracted MFCC (Mel frequency Cepstral Coefficients) features.
● (MFCC) are used for Keyword Spotting (KWS) because they mimic the way humans perceive sound, reduce dimensionality, are invariant to scale and pitch changes, capture temporal dynamics, and provide robustness to noise. Their proven effectiveness in speech tasks and compatibility with deep learning models make them a reliable choice for representing speech signals in KWS applications

![Screenshot 2024-02-17 114641](https://github.com/PVHarika/Keyword-Spotting-/assets/147228955/7e31f857-d57b-454c-a770-6bec53db55d7)

# MODELS:
**CNN** - Convolutional Neural Network : By processing 1-Dimensional representations of audio such as MFCC or Spectrogram, CNN identifies temporal features that are important for accurate predictions. The layers like pooling, Normalization, Drop-out enhances the efficiency, with output layers characterized by softmax activation function to assign probabilities to different output classes. By using loss function, we will backtrack and increase the efficiency.

![Screenshot 2024-02-17 115123](https://github.com/PVHarika/Keyword-Spotting-/assets/147228955/4bc3dda4-a5aa-4439-91f6-c76250387f5b)

# WEB APPLICATION 
To complete the project, we have concluded it with a working UI built using Python and Flask.
This UI takes input as a .wav audio file, and then when we enter the Transcribe button, it gives the output [predicted class].

![image](https://github.com/PVHarika/Keyword-Spotting-/assets/147228955/ede79741-f8e1-4408-a19c-d363cc83f16c)

![image](https://github.com/PVHarika/Keyword-Spotting-/assets/147228955/533fa88e-1ba2-47ce-8745-42259907005d)
