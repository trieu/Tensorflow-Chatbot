# Tensorflow Chatbot
Tensorflow Chatbot Demo by @Sirajology on [Youtube](https://youtu.be/SJDEOWLHYVo)

Overview
============
This is the full code for 'How to Make an Amazing Tensorflow Chatbot Easily' by @Sirajology on [Youtube](https://youtu.be/SJDEOWLHYVo). In this demo code, we implement Tensorflows [Sequence to Sequence](https://www.tensorflow.org/versions/r0.12/tutorials/seq2seq/index.html) model to train a
chatbot on the [Cornell Movie Dialogue dataset](https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html). After training for a few hours, the bot is able to hold a fun conversation.


Dependencies
============
* numpy
* scipy 
* six
* tensorflow (https://www.tensorflow.org/versions/r0.12/get_started/os_setup.html)

Use [pip](https://pypi.python.org/pypi/pip) to install any missing dependencies


Usage
===========

To rebuild them:
* mkdir tensorflow_chatbot/data
* cd tensorflow_chatbot/data
* Get https://people.mpi-sws.org/~cristian/data/cornell_movie_dialogs_corpus.zip, put the *.txt files in this new data/ dir.
* git clone https://github.com/suriyadeepan/datasets.git
* Edit datasets-master/seq2seq/cornell_movie_corpus/scripts/prepare_data.py and uncomment the last lines so prepare_seq2seq_files executes.
* python datasets-master/seq2seq/cornell_movie_corpus/scripts/prepare_data.py
* This makes {train,test}.{enc,dec}

These files are just lines of text. I guess matching line numbers between enc and dec are conversation pairs.

To train the bot, edit the `seq2seq.ini` file so that mode is set to train like so

`mode = train`

then run the code like so

``python execute.py``

To test the bot during or after training, edit the `seq2seq.ini` file so that mode is set to test like so

`mode = test`

then run the code like so

``python execute.py``


Credits
===========
Credit for the vast majority of code here goes to [suriyadeepan](https://github.com/suriyadeepan). I've merely created a wrapper to get people started. 
