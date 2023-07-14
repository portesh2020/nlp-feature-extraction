## Author
Hannah Portes


## Files
Name | Purpose
--- | ---
``feature_extraction_analysis.ipynb`` | Notebook containing all the code for task 1
``classification_experiments.ipynb`` | Notebook containing all the code for task 2

## Usage
The feature analysis notebook contains code for extracting the pitch and intensity arrays from all the audio files provided. 
The min, max, mean of pitch and te min, max, mean of intensity are calculated by grouping speakers and normalizing the array values extracted, before going row by row and calculating the mean/min/max of these values. This process is also detailed in the pdf corresponding to part1 feature extraction and analysis.

The classification experiments notebook contains code using opensmile to extract features from all of the audio files provided.

### Program Run Instructions
The notebooks can be run as long as the paths correspond to the correct files.

The notebooks require the audio samples to be in folder titled 'hw3_speech_files'. The program looks for this directory and then extracts audio features from all files within that folder ending in the extension .wav. Similarly, the speaker and emotion names are extracted from the title of the files so this naming convention must be maintained as well (speaker_num_emotion_...wav).

```
ex: cc_001_anxiety_910.77_May-twenty-third.wav
```

The classification experiments require the OpenSmile SMILExtract to be in the directory opensmile (I moved it from deep within the path ``build/progsrc/...``). The config file used remains at the path ``opensmile/config/is09-13/IS09_emotion.conf`` and the features extracted are output to ``opensmile_features.csv``. These are all set in the first 5 cells of the notebook and can be modified accordingly.


## Notes
- As specified in the hw instructions, opensmile is cloned and build using the following commands:

```
git clone https://github.com/audeering/opensmile.git
cd opensmile/
bash build.sh 
```

These are not in the .ipynb file as I ran these commands in my terminal before working on the feature extraction. Once the opensmile code is cloned and configured following the instructions above, the notebook will run.