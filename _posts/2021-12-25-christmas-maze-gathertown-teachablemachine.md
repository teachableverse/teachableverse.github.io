---
date: 2021-12-25 12:00:00
layout: post
title: Christmas Maze on Gather Town using Teachable Machine
subtitle: Gather Town and Teachable Machine
description: This verse is a space where you can enjoy the Christmas maze together. This space was implemented on the gather town, and control definition is possible with the desired behavior through a teachable machine.
image: https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_play.gif
optimized_image: https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_title_0.jpg
category: game
tags:
  - gathertown
  - teachablemachine
  - game
author: Taeyoung Kim
---
Gather Town is a place where you can create a map with a metaverse video conferencing platform and communicate with various activities and communication through avatars in that map. There are many cases where Gather Town is used as a playground, and one of them is to play a maze search game.

It is not recommended to find the maze directly through mouse control because it finds the path to the destination on its own through the pathfinding Algorithm. Like finding a maze made of wood or the like offline, it can be implemented on Gather Town similarly, and then you can play a maze game using a teachable machine to define the still, up/down, and left/right behavior.

<iframe width="100%" height="400" src="https://www.youtube.com/embed/06PkLEtzNDM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Features
* Multiple people can come online and play against each other.
* People with physical disabilities can easily participate in the game because they can learn with the behavior they want. 
* You can actually enjoy it as if you were playing a maze pathfinding game like an offline space.

### Preparation

#### To make maze on Gather Town

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_gathertown.jpg)

#### To define behaviors using Teachable Machine

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel.jpg)

The wef1yJup2 model provided by default has been learned as follows.

|stay|up|down|right|left|
|---|---|---|---|---|
|![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_stay.jpg)|![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_up.jpg)|![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_down.jpg)|![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_right.jpg)|![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_left.jpg)|

### How to play

1. Access the pre-made maze town. : https://gather.town/app/4BDf97jEEOpc6l8c/Christmas%20maze
1. Download the source code from the following github address. : https://github.com/teachableverse/christmas-maze-gathertown-teachablemachine
1. Run Python program app.py. >> python app.py
1. Enter 127.0.0.1:5001 in the Chrome browser.
1. Click the Load button to load the teachable machine model (wef1yJup2) that has already learned the behaviors. If you want to load your own model, enter the ID of the model and click the Load button.
1. Click the Gather Town window so that the key message can be entered into Gather Town.
1. Control Gather Town's avatar with predefined behaviors using cam.

### How to define your own behavior.

You can train the machine learning model in the following order with the Teachable Machine Pose Project.

1. Access https://teachablemachine.withgoogle.com/ to create a Pose Project.

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_0.jpg)

2. Collect data samples by adding classes in the order of stay-up-down-right-left.

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_1.jpg)

3. Click the Train Model to train the model with the collected dataset.

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_2.jpg)

4. Make sure that the model you trained is functioning normally.

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_3.jpg)

5. Click the [Upload my model] button to upload the trained model to the cloud.

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_4.jpg)

6. Check the uploaded model path and id. 

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_5.jpg)

7. Enter the id into the input form on the page "http://127.0.0.1:5001/" and click [Load] to apply the trained model.

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_6.jpg)

### More
* Go to github [here](https://github.com/teachableverse/christmas-maze-gathertown-teachablemachine)