---
layout: page
title:  "Cellular Automata for Image Classification"
subtitle: "Self-organising systems"
date:   2021-02-05 21:21:21 +0530
permalink: 'cellular_automata'
categories: ["general"]
---

Here we study how individual agents with local information can collectively perform a global task. 

Consider this simple example: you are a single pixel in an 1080p picture of a leopard, you know your color, intensity and let's assume you can also see the same information about your immediate neighbours (picture the 3x3 neighborhood of pixels centered around you). 

{% comment %}
Might you have an include in your theme? Why not try it here!
{% include my-themes-great-include.html %}
{% endcomment %}

![A 1080p image of a leopard with zoom on a subset of its pixels](/assets/images/leopard-zoom.jpg "A 1080p image of a leopard with zoom on a subset of its pixels")
<!-- <span>Photo by <a href="https://unsplash.com/@esu?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Adaivorukamuthan</a> on <a href="https://unsplash.com/s/photos/leopard?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a></span> -->

Based only on this local information, could you ever find out that you are part of a bigger leopard image? Certainly not! After all, that particular local information could be part of a cat's picture, a scarf, or even something else completely different.

But what if all the pixels can get together and devise a clever strategy to communicate with each other to reach consensus on what the full image is all about? Is there even such a communication strategy? 

Instead of designing ourselves this strategy we allow it to be automatically learned with the tools of deep learning.

But first, it's worthwile explaining what are Cellular Automata.

# From (simple) rules to (unpredictable) behavior

Simple definition of a Cellular Automata

But it's best to understand by two well known examples

## Wolfram's simple one dimensional automata

This is the simplest cellular automata. Cells (pixels) can only have binary values. and are one-dimensional

For this simple case, there are actually only # possible rules. Most of the rules are not interesting, but some get quite interesting. 

Rule 30 used for random number generator

Link More details
Link try it out

## Conway's game of life

1. Any live cell with two or three live neighbours survives.
1. Any dead cell with three live neighbours becomes a live cell.
1. All other live cells die in the next generation. Similarly, all other dead cells stay dead.

Link More details
Link try it out

# From (desired) behavior to (learned) rules

Recent advances in Machine Learning has allowed end-to-end training 

We expand the state of each automata with communication channels

One type of deep net, the convolutional neural network is suited for cellular automata if we consider filters of size 3x3 in the first layer and 1x1 in the subsequent layers.

We then train the weights of the conv2d with backpropagation.

We can use tensorflow to do this and the code is online.

In this work we start with a simpler problem. Count digits

## Count Digits

Explain the task, motivate why it's interesting

Show a video of the agents performing the task

Maybe explain Mutate Training, Random initialisation

## XOR

Explain the task, motivate why it's interesting

Show how the model is different

See it in action

## Fruit Classification

We tested also for simple image classification.

Explain the task, why we lost colour

Show the results

# Conclusion

Neural networks vs Cellular Automata

# Credits

Distill

