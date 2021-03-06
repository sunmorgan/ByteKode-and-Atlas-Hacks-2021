# Privacy Guard
### Making Privacy More Accessible

## What It Does
This is a tool that auto-detect faces, license plates(cars), and paperwork(confidential/personal documents), and blurs them out. This is generally used for individuals who have to edit videos/photos that are going to be posted online. Privacy is quite valued to many people, and therefore the use of this app would greatly help to achieve a high level of privacy. 

## What Inspired Me
My cousin is a video editor for a club at his university, and he often has to stay up late to blur out sensitive content e.g) school work, license plates on cars. I then wanted to create something that could automate those tasks for him, and I believe the use of object detection is prominent to complete this task. 

Apart from that, I'm an avid youtube watcher and I often see my favorite content creators struggle manually edit out objects that relate to privacy concerns. Therefore creating an app like this could easily help them to achieve their goal.

## What I Used
When doing this, I had two options: one was to use YOLO from TensorFlow and the other one was obviously OpenCV. After careful considerations, I decided that I will not be implementing deep learning into this project and will use OpenCV by utilizing cascade classifiers. Besides the default classifier made by OpenCV to detect faces, I trained my own cascade classifier for both the license plate and document detector. I've decided to abort making a GUI due to a one-man team and will be using a user-terminal interface. 

## Accomplishments I'm Proud Of
Training a cascade classifier that works! After experiencing many unsuccessful stages of training my own classifier, I had a pinch of wanting to migrate to making a website as it'd be easier. But I persevered and captured my mistake through each unsuccessful attempt and finally come to my final product that could detect both license plates and documents. 

## Challenges I Ran Into
Before training a successful cascade classifier, I've failed a couple of dozen times; and I could not find out the cause. So I had to list out all the possible factors that influence the success rate and eliminate them by implementing them one by one. Through the process of elimination, I came to two conclusions. **Number 1:** When choosing positive/negative cases, the positives have to be very similar in terms of the general features (shape, size, color, etc) if you decide to train with a limited amount of cases (anything below 500). And here comes **Number 2:**, the vice versa of 1, if you decide to have positive test cases that have a large diversity amongst its features, you should have a large number of cases (at least 1000). 

## What's Next For Privacy Guard
The user's hands-on experience with this app is very limited because they have to process their image/video through a terminal. I am planning to create a website that hooks up the code by using frameworks like Flask or Django. 

## What I learned
Training my own cascade classifier. I've only used the default classifiers created by OpenCV for side projects I made previously; so training a cascade classifier was an undoubtedly difficult step to take. Through my attempts, I've gained experience on the ratio positive and negative cases should be, and the quality for each folder.
