char-rnn-tensorflow
===

Fork of [char-rnn-tensorflow](https://github.com/sherjilozair/char-rnn-tensorflow) trained on 28 essays and books sourced from [Project Gutenberg](https://www.gutenberg.org/) pertaining to aesthetics, beauty, and arts. All books in txt format available in [data/onaesthetics/Orig](https://github.com/hsab/char-rnn-tensorflow/tree/master/data/onaesthetics/Orig) folder.

[![Join the chat at https://gitter.im/char-rnn-tensorflow/Lobby](https://badges.gitter.im/char-rnn-tensorflow/Lobby.svg)](https://gitter.im/char-rnn-tensorflow/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Coverage Status](https://coveralls.io/repos/github/sherjilozair/char-rnn-tensorflow/badge.svg)](https://coveralls.io/github/sherjilozair/char-rnn-tensorflow)
[![Build Status](https://travis-ci.org/sherjilozair/char-rnn-tensorflow.svg?branch=master)](https://travis-ci.org/sherjilozair/char-rnn-tensorflow)

Multi-layer Recurrent Neural Networks (LSTM, RNN) for character-level language models in Python using Tensorflow.

Inspired from Andrej Karpathy's [char-rnn](https://github.com/karpathy/char-rnn).

## Books & Essays

* Aesthetical Essays of Friedrich Schiller by Friedrich Schiller
* Ancient Art and Ritual by Jane Ellen Harrison
* Aristotle on the art of poetry by Aristotle
* Homer and Classical Philology by Friedrich Wilhelm Nietzsche
* Ion by Plato
* Kant's Critique of Judgement by Immanuel Kant
* Laughter An Essay on the Meaning of the Comic by Henri Bergson
* Lectures on the true, the beautiful and the good by Victor Cousin
* Literary and Philosophical Essays French, German and Italian by Immanuel Kant et al
* Modern Painters, Volume 1 (of 5) by John Ruskin
* Modern Painters, Volume 2 (of 5) by John Ruskin
* Modern Painters, Volume 3 (of 5) by John Ruskin
* Modern Painters, Volume 4 (of 5) by John Ruskin
* Modern Painters, Volume 5 (of 5) by John Ruskin
* On the Laws of Japanese Painting
* The Birth of Tragedy by Friedrich Wilhelm Nietzsche
* The Case Of Wagner, Nietzsche Contra Wagner, and Selected Aphorisms by Nietzsche
* The Philosophy of Fine Art, volume 1
* The Philosophy of Fine Art, volume 2
* The Philosophy of Fine Art, volume 3
* The Philosophy of Fine Art, volume 4
* The Photoplay by Hugo Münsterberg
* The Poetics of Aristotle by Aristotle
* The Principles of Aesthetics by De Witt H Parker
* The Psychology of Beauty by Ethel Puffer Howes
* The Republic by Plato
* The Sense of Beauty Being the Outlines of Aesthetic Theory by George Santayana
* Thoughts on Art and Life by da Vinci Leonardo

## Generated Examples

Tained with `rnn_size=128` and `num_layer=2`

```python sample.py --save_dir=.\data\onaesthetics\save128_3\ --prime="Read me" --sample=2```

Read men and he and on account of the "poet seem to present it by great notion of the interest of beauty and modern subject and consciousness is consequently distinctions in the expression of the latter life that we have we must have consequently the whole of a definite and the real and subject of such a conception of its life like kinds of its content is a conception that reality of every heart and visible to give the form in the most visible point of qualities of his Beautiful sense, and in other det

```python sample.py --save_dir=.\data\onaesthetics\save128_3\ --prime="Read me" --sample=1```

Read men and when a fine more than all our Ashernals, the opposite tashing you are not only to detect itself his generally, a depicting as second. Let us prederiness, as heiling here?   "O, cold that he art be even necessitation of a flashed it from its real world, that is that of their unfeticular than sound is great front which right things are unlimiterned sense; in spite to the Uté and his will, when we termed else on earth, which offer them Principle, is—the aesthetical judgement called with surpa

## Basic Usage
To train with default parameters on the tinyshakespeare corpus, run `python train.py`. To access all the parameters use `python train.py --help`.

To sample from a checkpointed model, `python sample.py`.

## Datasets
You can use any plain text file as input. For example you could download [The complete Sherlock Holmes](https://sherlock-holm.es/ascii/) as such:

```bash
cd data
mkdir sherlock
cd sherlock
wget https://sherlock-holm.es/stories/plain-text/cnus.txt
mv cnus.txt input.txt
```

Then start train from the top level directory using `python train.py --data_dir=./data/sherlock/`

A quick tip to concatenate many small disparate `.txt` files into one large training file: `ls *.txt | xargs -L 1 cat >> input.txt`

## Tensorboard
To visualize training progress, model graphs, and internal state histograms:  fire up Tensorboard and point it at your `log_dir`.  E.g.:
```bash
$ tensorboard --logdir=./logs/
```

Then open a browser to [http://localhost:6006](http://localhost:6006) or the correct IP/Port specified.

## Contributing
Please feel free to:
* Leave feedback in the issues
* Open a Pull Request
* Join the [gittr chat](https://gitter.im/char-rnn-tensorflow/Lobby)
* Share your success stories and data sets!
