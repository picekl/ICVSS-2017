
# Monday

## Vladlen Koltun: Learning to Act with Natural Supervision

Vladlen Koltun             | Learning to Act
:-------------------------:|:-------------------------:
![](https://i.imgur.com/tfo5h60.jpg)  |  ![](https://i.imgur.com/ycoCny7.jpg)



### Key Messages

* Reinforcement Learning 
   * Reinforcement learning is learning what to do - how to map situations to actions - so as to maximise a numerical reward signal.
* Why is it called Reinforcement ? —> Conditioned reflexes - Pavlov 1927
   * reward and punishment 
   * History (Pavlov and the dog , Skinner and pigeons - behaviorism -> animal behavior can be explained in terms of conditioning)

* Natural Supervision Example
   * act and observe the consequences
   * learn to predict the consequences of actions
   * Learn to map observarion x action -> future observation


* LEARNING TO ACT  (Markov decition proces)
* Problems:
    * State - “Grid world” don’t work with 3D real world situations (“perspective”)
    * Reward - “What is the reward for life?”, 
    * Discounting - Its extremely aggressive. In reality you can chose something with smaller discount
    * Markov Assumption - No history


[comment]: <> (![](https://i.imgur.com/JdG4etm.jpg)


## [Emilio Frazzoli: On nuTonomy's Vision for Autonomous Driving](http://iplab.dmi.unict.it/icvss2017/Lectures/Frazzoli.pdf)

Emilio Frazzoli            |  Title
:-------------------------:|:-------------------------:
![](https://i.imgur.com/786688V.jpg) |  ![](https://i.imgur.com/RqQbP3T.jpg)


### Key Messages

* Mobility as a service is the way to go
    * Easier to scale / unroll
    * Cost efficient for consumer *and* provider
    * Controlled Environoment
* *Levels* of autonomy is misleading
    * OEMs try to increasy autonomy step by step
    * MaaS (AVs as a service (MaaS)) approach allows to unroll by scaling up the scope
* Utilize prior Knowledge where applicable
    * *Rules of the Road* don't need to be learned
    * Use formal logic for decision making
    * Utilize graph theory for planning
    * Combine traditional methods with learning


| Column 1 | Column 2 | Column 3 |
| -------- | -------- | -------- |
| ![](https://i.imgur.com/B0GvRRk.jpg) | ![](https://i.imgur.com/d8aeP6S.jpg) | ![](https://i.imgur.com/DvVrNv1.jpg)
| ![](https://i.imgur.com/wGfH8oH.jpg) | ![](https://i.imgur.com/exo2lm7.jpg) | ![](https://i.imgur.com/Oh0sQ4O.jpg)

## [Hao Li: Digital Human Teleportation](http://iplab.dmi.unict.it/icvss2017/Lectures/Li.pdf)

Hao Li            |  Title
:-------------------------:|:-------------------------:
![](https://i.imgur.com/r34SmqB.jpg)  | ![](https://i.imgur.com/7fsrfzt.jpg)

### Key Ideas

* Allow realistic digital communication
    * with everyday hardware
* Requires to capture fine grane details
    * to transport non-verbal aspects of communication
* Use deep learning to infer those details
    *  instead of expensive sensoring equipment


# Tuesday

## [Trevor Darrell: Adaptive Representation Learning](http://iplab.dmi.unict.it/icvss2017/Lectures/Darrell.pdf)

Trevor Darrell       |  Title
:-------------------------:|:-------------------------:
![](https://i.imgur.com/qJjxRu9.jpg) | ![](https://i.imgur.com/dYwScng.png)

### Key Ideas:

* Domain adaptation
    * Use adversial network for cross-domain adaptation
    * Force the network to learn a representation which is indistinguisable between two domains
    * (future project?)
* Natural Supervision
* Curious learning
    * Use loss as reward in RL
* Visual Explanations
    * Use attention to make model interpretable


## Sanja Fidler: Learning Embettings of Images and Language

Sanja Fidler      |  Learning Embettings of Images
:-------------------------:|:-------------------------:
![](https://i.imgur.com/8McDzDy.jpg) | ![](https://i.imgur.com/VjOf4W0.jpg)


[comment]: <> (![](https://i.imgur.com/oBlXl2u.jpg)

 
 
 ### Key Ideas: (No slides avaible yet...)
 * Use word2vec (or similar) to learn embetting for words
 * RNNs for sequential models
 * Tasks:
     * Image Captioning
     * Classification using description (zero short)


# Wednesday

## Vittorio Ferrari: Weakly Supervised Learning

Vittorio Ferrari     |  Learning Embettings of Images
:-------------------------:|:-------------------------:
![](https://i.imgur.com/Dm2dWgo.jpg) | ![](https://i.imgur.com/Q4PdK0V.jpg)


### Key Points: (No slides avaible yet...)

* Weakly supervised learning: Learn from a lower degree of supervision 
* Semi-supervised learning: combine labeled unlabeled data (useful project?)
* Utilize that different combinations of labels appear
    * Face recoginition example
    * Training: EM
* [Weakly Supervised Deep Detection Networks](https://arxiv.org/abs/1511.02853)
* One point per class (Use object model)

## Ross Girshick: From Visual Perception to Visual Reasoning

Ross Girshick             |  From Visual Perception to Visual Reasoning
:-------------------------:|:-------------------------:
![](https://i.imgur.com/BMtDN6e.jpg) | ![](https://i.imgur.com/VjL5ddd.jpg)

### Key Ideas:

* Respect Variation:
    * Translational Variation
    * Rotational Variation
    * Scale Variation
    * Deformation Variation 
    * Intra-class Variation
* Problem might be Invariances or Equivariance w.r.t. variation
* Look at old papers
    * You might find good ideas
* [Mask-RCNN](https://arxiv.org/abs/1703.06870)
    * Modularised Approach
    * [Feature Pyramid Networks for Object Detection](https://arxiv.org/abs/1612.03144)
* Kluger Hans & Visual Question Answering
    * is VQA only nearest neighboor?
    * How do we know our models are as sophisticated as we think
* [Diagnosing Errors in Object Detectors](http://dhoiem.web.engr.illinois.edu/projects/detectionAnalysis/)
    * Useful Error diagnosation tool
* [CLEVR: A Diagnostic Dataset for Compositional Language and Elementary Visual Reasoning](https://arxiv.org/abs/1612.06890)
    * Dataset for analysing VQA


# Thursday

## Abhinav Gupta: Self-supervised Learning of Visual Representations

Abhinav Gupta            |  Self-supervised Learning of Visual Representations
:-------------------------:|:-------------------------:
![](https://i.imgur.com/gnUVzax.jpg) | ![](https://i.imgur.com/Np9WDgy.jpg)

### Key Ideas

* Use auxiliary tasks as pretraining
* For classification the following tasks are useful:
    * predict color channel (given RGB channel)
    * predict relative positions of text
    * *jigsaw puzzl* predict position of patches
    * predict content of hole
* Kluger Hans Issue (shortcuts)
    * low level image structures (edges)
    * camera artifacts
* Solution: Jitter input
    * Augment position
    * drop color channel
* Natural supervised training not yet competative with ImageNet pretraining
    * (ImageNet labels as *natural supervision for some tasks?*)
* Validate weakly supervision
    * only finetune few layers
    * use view data



| Column 1 | Column 2 | Column 3 | Column 4 |
| -------- | -------- | -------- | -------- |
| ![](https://i.imgur.com/M74PpBj.jpg)  | ![](https://i.imgur.com/svnlJ7i.jpg)  | ![](https://i.imgur.com/6ZyqlGI.jpg) | ![](https://i.imgur.com/IJO7Yjq.jpg)

## Jan Peters: Learning Visuomotor Skills in Robotics

Jan Peters                 |  Learning Visuomotor Skills in Robotics
:-------------------------:|:-------------------------:
![](https://i.imgur.com/LfxgKxW.jpg) | ![](https://i.imgur.com/Km3OHZ9.jpg)


### Key Message (No slides avaible yet...)

* Machine Learning is not Robot Learning
    * Robot Learning has its own unique challanges
* Use prior knowledge (e.g. about physics) where avaible
    * we have very good models, e.g. for motion planning
    * not everythink needs to be learned from scratch




# Friday

## Raquel Urtasun: Towards Affordable Self Driving Cars

Raquel Urtasun          |  Towards Affordable Self Driving Cars
:-------------------------:|:-------------------------:
![](https://i.imgur.com/96U4tWh.jpg) | ![](https://i.imgur.com/oVCR8xl.jpg)

### Key Points: (No slides avaible yet...)

* combine computer vision knowledge with 
    * e.g. solve stereo by computing matchings
    * use flow for detection / segmentation
    * [geometric aware cnn](http://www.cs.toronto.edu/deepLowLevelVision/)
* prediction (of road user behaviour) is an important task
* Visual Odometry (localization / mapping) needs more research
* Cityscapes offers poor meta-data
* 3D detection is required



| Column 1 | Column 2 | Column 3 |
| -------- | -------- | -------- |
| ![](https://i.imgur.com/8awqYEc.jpg) | ![](https://i.imgur.com/evRO0wi.jpg) | ![](https://i.imgur.com/Sbz158o.jpg) |




## Andrew Fitzgibbon: Learning Visuomotor Skills in Robotics

Andrew Fitzgibbon          |  Optimiztion
:-------------------------:|:-------------------------:
![](https://i.imgur.com/1vNL2qr.jpg) | ![](https://i.imgur.com/sB9M0p6.jpg) 



### Key Points: (No slides avaible yet...)

* Finding solution *fast* (*speed*) is the key goal
* To find global optima, search for local optima
    * on some problem spaces (quasi-convex) reaching global optima is garantied
    * otherwise use random research
* optimization is an ongoing field of research
* better optimization algorithms can improve machine learning


| Column 1 | Column 2 | 
| -------- | -------- |
| ![](https://i.imgur.com/H5lK3tC.jpg) | ![](https://i.imgur.com/hYCp120.jpg) | 
