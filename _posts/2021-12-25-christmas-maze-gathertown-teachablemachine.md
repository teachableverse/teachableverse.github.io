---
date: 2021-12-25 12:00:00
layout: post
title: Christmas Maze on Gather Town using Teachable Machine
subtitle: Gather Town and Teachable Machine
description: This verse is a space where you can enjoy the Christmas maze together. This space was implemented on the gather town, and control definition is possible with the desired behavior through a teachable machine.
image: https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_title_0.jpg
optimized_image: https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_title_0.jpg
category: game
tags:
  - gather town
  - teachable machine
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
|![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_stay.jpg)|![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_up.jpg)|   |![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_down.jpg)|![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_right.jpg)|
|![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_left.jpg)|

#### Usage

1. 미리 만들어놓은 미로 게더타운(https://gather.town/app/4BDf97jEEOpc6l8c/christmas%20maze)에 접속합니다.
1. gihtub 주소(https://github.com/teachableverse/christmas-maze-gathertown-teachablemachine)에서 소스코드를 다운로드 받습니다. 
1. 파이썬 프로그램인 app.py를 실행시킵니다. >> python app.py
1. 크롬 브라우저 주소창에 127.0.0.1:5001를 입력합니다.
1. Load 버튼을 클릭하여 이미 행동을 학습시킨 티처블머신 모델(wef1yJup2)을 로딩합니다. 만약 직접 행동을 정의한 모델이 있다면, 해당 모델의 아이디를 1. 입력한 후 Load 버튼을 클릭합니다.
1. 키 메시지가 게더타운에 입력될 수 있도록 미로 게더타운 창을 클릭합니다.
1. 미리 정의된 행동으로 게더타운의 아바타를 제어합니다.

#### How to define your own behavior.

Teachable Machine의 Pose Project로 머신러닝 모델을 아래 순서로 학습십니다. 

1. https://teachablemachine.withgoogle.com/ 에 접속하여 Pose Project을 생성합니다.

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_0.jpg)

2. stay-up-down-right-left 순으로 class를 추가하여 데이터 샘플을 수집합니다.

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_1.jpg)

3. Train Model을 클릭하여 수집한 데이터셋으로 모델을 학습시킵니다.

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_2.jpg)

4. 학습한 모델이 정상적으로 작동되는 지 확인합니다.

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_3.jpg)

5. [Upload my model] 버튼을 클릭하여 학습한 모델을 클라우드에 업로드합니다.

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_4.jpg)

6. 업로드 된 모델 경로 및 id를 확인합니다. 

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_5.jpg)

7. 확인한 id를 “http://127.0.0.1:5001/” 페이지의 입력 폼에 입력한 후 [Load] 클릭하면 학습한 모델이 적용됩니다.

![img](https://teachableverse.github.io/warehouse/2021-12-25-christmas-maze-gathertown-teachablemachine_tmmodel_training_6.jpg)
