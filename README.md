# Detection of fillers in conversational speech

## About fillers

This work is a NLP master's degree project aiming at improving ASR systems, in particular in the specific task of detecting fillers in spontaneous speech. 

Fillers are a specific type of disfluencies. Disfluencies can be defined as interruptions in normal flow of speech which make utterances longer without adding semantic information. Fillers, in particular, are vocalizations, like “uhm”, “eh”, “ah” etc., which fill the time that should be occupied by a word (generally in correspondence of hesitations, uncertainty or attempts to hold the floor).


## Approach
A neural network approach has been attempted. Using the corpus [CallHome](https://catalog.ldc.upenn.edu/LDC97S42), we performed a forced alignment task between transcriptions and audio files using [Montreal Forced Aligner](https://montreal-forced-aligner.readthedocs.io/en/latest/). This alignment allowed us to automatically assign tag to each frame of the speech, choice being between _silence_, _speech_, and _filler_. 
Finally we fed a sequence tagger Neural network with the sequences of Mel-frequency cepstral coefficients extracted over the above-mentioned frames.

## Notebook
To run the notebook, you will need to install before hand the following python libraries: Pydub, soundfile, textgrids, pandas, torch, torchaudio, and sklearn.
Also, the following softwares are needed: [Montreal Forced Aligner](https://montreal-forced-aligner.readthedocs.io/en/latest/) (for the forced alignment process), [Sox](http://sox.sourceforge.net/) for the stereo-mono conversion.
Afterward, the notebook is ready to run. 
