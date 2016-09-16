####Overview

A project that trains a LSTM recurrent neural network over a dataset of MIDI files. 

More information can be found on the [Yoav's blog post](http://yoavz.com/music_rnn/).

*Warning: Some parts of this codebase are unfinished.*

####Dependencies


* [Tensorflow](https://github.com/tensorflow/tensorflow) ! **(0.8.0)**
* [Numpy](http://www.numpy.org/)
* [Python Midi](https://github.com/vishnubob/python-midi.git)
* [Mingus](https://github.com/bspaans/python-mingus)
* [Matplotlib](http://matplotlib.org/)
* [Ipython](https://ipython.org/) (optional)

*requirements.txt includes all the dependencies except **tensorflow***

####Installation

`git clone https://github.com/hiorws/rnn-music-generating.git`

`cd rnn-music-generating/`

`virtualenv venv`

`source venv/bin/activate`

`pip install -r requirements.txt`

For Ubuntu/Linux 64-bit, CPU only:

`pip install --upgrade https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-0.8.0-cp27-none-linux_x86_64.whl`

For Mac OS X, CPU only:

`pip install --upgrade https://storage.googleapis.com/tensorflow/mac/tensorflow-0.8.0-py2-none-any.whl`

If you're using Mac OS X:

`echo "backend: MacOSX" >> ~/.matplotlib/matplotlibrc`



####Basic Usage

- `mkdir data && mkdir models`
- Download the dataset [Nottingham MIDI dataset](http://www-etud.iro.umontreal.ca/~boulanni/Nottingham.zip) and unzip to `data/Nottingham`
- Run `python nottingham_util.py` to generate the sequences and chord mapping file to `data/nottingham.pickle`
- Run `python rnn.py --run_name YOUR_RUN_NAME_HERE` to start training the model. Use the grid object in `rnn.py` to edit hyperparameter configurations.
- Run `python rnn_sample.py --config_file generated_config_by_you` and `best.midi` will be generated in your current directory!
- Enjoy and have fun! If you have any issue please share with me. If you have any suggestions please contribute and send a PR.
