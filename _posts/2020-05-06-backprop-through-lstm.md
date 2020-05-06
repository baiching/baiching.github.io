---
layout: post
title:  "Easiest way to backprogate through LSTM(long short term memory) using only numpy"
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

```code
00
```
hshshs

```bash
# "#" for comment
```
