####Overview

A project that trains a LSTM recurrent neural network over a dataset of MIDI files. 

More information can be found on the [Yoav's blog post](http://yoavz.com/music_rnn/).

*Warning: Some parts of this codebase are unfinished.*

####Dependencies


* Numpy (http://www.numpy.org/) 
* Tensorflow (https://github.com/tensorflow/tensorflow) *(0.8.0)*
* Python Midi (https://github.com/vishnubob/python-midi.git)
* Mingus (https://github.com/bspaans/python-mingus)

*requirements.txt includes all the dependencies*


####Basic Usage


- `mkdir data && mkdir models`
- Download the dataset [Nottingham MIDI dataset](http://www-etud.iro.umontreal.ca/~boulanni/Nottingham.zip) and unzip to `data/Nottingham`
- Run `python nottingham_util.py` to generate the sequences and chord mapping file to `data/nottingham.pickle`
- Run `python rnn.py --run_name YOUR_RUN_NAME_HERE` to start training the model. Use the grid object in `rnn.py` to edit hyperparameter
   configurations.
