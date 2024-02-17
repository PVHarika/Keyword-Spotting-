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
