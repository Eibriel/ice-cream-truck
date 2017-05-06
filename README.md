# Ice Cream Truck bot
This chatbot allows you to place an order of Ice Cream in a [Random Access Navigation](https://medium.com/assist/theres-a-dozen-ways-to-order-a-coffee-why-do-dumb-bots-only-allow-one-27230542636d) way, using a Memory Neural Network.

Entry for machine learning tutorial [How to Make a Chatbot - Intro to Deep Learning #12](https://www.youtube.com/watch?v=t5qgjJIBy9g)


## Dependencies
- python 3
- tensorflow
- keras
- h5py (For saving and loading the model)
- requests (For Telegram support)

## Running
To run the command line interface, just type:
`python chatbot.py`
The bot will use the included pre trained model, if you want to train your own remove the file `model.hdf5`

## CLI interface
Interaction example:

```
>add chocolate
>change chocolate for cherry
>add coffee
>done


Your order: cherry, coffee 🍦
```

## Telegram interface
In order to use a Telegram bot as your interface:

- Install [Telegram](https://telegram.org)
- Add BotFather to your contancts: https://t.me/BotFather
- Use the `/newbot` command and follow the instructions
- On the code duplicate the file `sample_config.py` to `config.py`
- From BotFather copy the bot token to `config.py`
- Run the chatbot with the following parameter `python chatbot.py telegram`

Done! You can now add your bot to your contacts and order your Ice Cream

My demo on Telegram: https://t.me/eibriel_icecream_bot

![Telegram Demo](telegram.jpg)


## Installing

If you are familiar with virtualenv create a new one after cloning the repo.

I am naming my env bobo:

```bash
virtualenv -p /usr/local/bin/python bobo
```

If you are using bash activate your env:

```bash
. bobo/bin/activate
```

Fish users just use the fish version.

```fish
. bobo/bin/activate.fish
```

After activating you get a similar prompt:

```fish
(bobo) ~/c/s/ice-cream-truck (master ⚡☡=)
```

Installing libraries:

```bash
pip install -r requirements.txt
```

Startung up the bot:

```fish
(bobo) ~/c/s/ice-cream-truck (master ⚡→☡=) python chatbot.py
Using TensorFlow backend.
Missing config.py, no Telegram support
-
('Vocab size:', 22, 'unique words')
('Story max length:', 30, 'words')
...
```

