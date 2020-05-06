---
layout: post
title:  "Easiest way to backprogate through LSTM(long short term memory using only numpy"
date:   2020-05-06 14:32:04 +0700
categories: [bash, linux, ubuntu]
---

I learned about lstm from [CS231n](http://cs231n.github.io/) which was great. But there was a lot that i didn't catch from lectures. Then I found
[this](http://colah.github.io/posts/2015-08-Understanding-LSTMs/) awesome blog. But when i went to implement LSTM backprop, i realized that i didn't
understand backprogattion. In [cs231n](http://cs231n.github.io/) course, i learned that there are two ways to apply backprop efficiantly,
1. Draw a graph on a piece of paper as you go and then just follow it backwards
2. Derive values by differentiating through the network

I found 1st one much easier to follow. Although it will get very messy very soon if we have very large net. But neural nets as just reuse same functions over and
over until finally apply a softmax or svm. So, if we calculate backprop for one unit, the process should be same for all other units.

You can use this some alternatives;


```bash
$ your-bash-command && aplay /path/to/sound.wav  # can also with *.ogg file.
```

```bash
$ your-bash-command && paplay /path/to/sound.ogg  # can also with *.wav file.
```

```bash
$ your-bash-command; spd-say "done"
```

```bash
$ your-bash-command && notify-send "done"  # without sound
$ your-bash-command && notify-send "Process completed" "Come back to the terminal, the task is over"
```

------------

And this script below is modification of that commands above.

1. Create the `notif-me.sh` file;

```bash
#!/bin/bash

notify-send "Process completed" "Come back to the terminal, the task is over"
spd-say "My lord, your process hasbeen complete."
```

2. Make it callable in `/bin`

```bash
sudo cp notif-me.sh /bin/notif-me;
```

3. Use it;

```bash
$ your-bash-command; notif-me

# or

$ your-bash-command && notif-me
```
