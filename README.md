# ProducerGAN
AI-generated audio samples for producers

Abstract: DCGAN (Radford et al., 2016) was created for learning to generate images. Donahue et al (2018) took this idea and applied it to audio to create WaveGAN. It is able to synthesize 1-4 second clips of birds, speech, piano, and drum sounds. We wondered if the same algorithm can be used for music, where a potential application includes the generation of creative audio samples for human producers to use. Some code from the WaveGAN project is used, as well as Tensorflow, Scipy, Matplotlib, and Librosa Python packages.

Method:
For each artist, songs were pulled randomly from YouTube, converted to mp3s, sliced into 4-second clips, and randomized again.

Results:
Tiesto (6500 iterations): Sample 1    Sample 2
Tiesto (10500 iterations): Sample 1    Sample 2
Justin Bieber (6500 iterations): Sample 1    Sample 2
Justin Bieber (10500 iterations): Sample 1    Sample 2

Challenges and Conclusion:
Due to slow compute time, only 1-second audio clips were generated
Longer and better audio is theoretically possible, but training may take >5 days on a standard CPU
