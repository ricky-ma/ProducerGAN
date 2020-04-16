# ProducerGAN
AI-generated audio samples for producers.
Created by **Ricky Ma**.

## Abstract
DCGAN (Radford et al., 2016) was created for learning to generate images. Donahue et al (2018) took this idea and applied it to audio to create WaveGAN. It is able to synthesize 1-4 second clips of birds, speech, piano, and drum sounds. I wondered if the same algorithm can be used for music, where a potential application includes the generation of creative audio samples for human producers to use. Initially trained on single artists/genres, ProducerGAN was able to generate audio of similar qualities. This can be extrapolated to include samples from multiple artists and/or genres to create music previously unheard of. Although its current output is limited, with sufficient time and computing power, this could be extended to produce full songs learned on many various artists and musical genres.

## Method
![Diagram](https://drive.google.com/uc?export=view&id=1K2C9XfEINt1bWLVghrf1b-4r7Hd2gkuC)

### Preprocessing:
Songs were pulled randomly from YouTube, converted to .wav files, and segmented into 4-second clips.
Each audio clip is then decoded and represented as a vector x, normalized, and transformed into uniform vectors Z.
Vectors Z are used to create the generator G using the WaveGAN algorithm.
Real discriminators D(x) are created from X and fake discriminators D(G(z)) from G(z).
### Training:
Discriminator D and generator G are optimized with the Adam Optimizer provided by Tensorflow.
For each iteration: D is optimized five times, then G is optimized once.
Weights for the generator are saved locally as the GAN trains.
Training does not end automatically: the number of iterations is controlled by the user.
### Generation:
Random vectors Z are created and fed into a trained generator G.
Vector G(z) is converted back into a waveform for playback.

## [Usage](https://drive.google.com/open?id=1jy1Dtu9H3vpJMyump0f7C_FYuDa17six)



