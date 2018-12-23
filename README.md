# ARKit

Most exciting frameworks released with iOS 11 is ARKit in WWDC17. With ARKit you can incorporate 3D data and objects into the physical environment of the user.

# Introducing ARKit
ARKit combines device motion tracking, camera scene capture, advanced scene processing, and display conveniences to simplify the task of building an AR experience. You can use these technologies to create many kinds of AR experiences using either the back camera or front camera of an iOS device.

## Understanding ARKit
ARKit offers you a high-level interface with powerful features. It’s supported on all devices with an A9 (or higher) processor. 

ARKit designed for iPhones and iPad that use the A9, A10 & A11 Processors.

iPhone 6s
iPhone 6s Plus
iPhone SE
iPad(2017)
iPhone 7
iPhone 7 Plus
iPhone 8
iPhone 8 Plus
iPhone X
ARKit provides the following capabilities:

## 1 - Tracking
Tracking enables us to track the phone in real-time and determine its position in the physical environment. It combines motion data, camera images and visual inertial iodometry to determine where the device is, as well as its orientation. ARKit uses a technique called visual-inertial odometry (VOI).


> Visual Odometry is the process of determining the position and orientation of a robot by analyzing the associated camera images. It has been used in a wide variety of robotic applications, such as on the Mars Exploration Rovers.


## 2 - Scene Understanding
Scene understanding helps us understand the environment around the device, providing attributes, properties and plane detection like floors, tables, and walls. To place objects onto planes, hit testing is being used. This is done by getting an intersection with the real-world topology. With light estimation, the object can be rendered to match the lightning of its surrounding.

## 3 - Rendering.
Data from images and sensors on the device can be provided as input in any renderer. For rendering with SceneKit and SpriteKit special ARViews are provided. Also, there is a Metal template for doing custom rendering.

## 4 - Light Estimates
ARKit also makes use of the camera sensor to estimate the total amount of light available in a scene and applies the correct amount of lighting to virtual objects.


## Basic ARKit Concepts
Let’s take a closer look at a few fundamental concepts 

## Session
ARKit is a session based framework. To start a new ARSession you need to provide it with an ARConfiguration. After that, you just need to run the session. This process runs at 60 frames per second and will start gathering information from the camera and the motion sensors. You can either poll for information or you can make use of the available session update delegates.

## Configuration
ARKit provides tracking based on device capabilities. Additional AR session features can be enabled or disabled through these configuration classes.

NOTE: ARConfiguration is an abstract class; you do not create or work with instances of this class.

 There are three supported configurations. 

1- ARWorldTrackingConfiguration It provides motion tracking like rotation of the device, position, plane detection and hit testing

2 - AROrientationTrackingConfiguration is a simpler configuration and it allows three degrees of tracking freedom. It detects only the device rotation

3 - ARFaceTrackingConfiguration on the other hand uses the front camera of the phone. It is used to track the movement and expression of the face of the user.

## Frames
A running AR session continuously captures video frames from the device camera. ARKit analyse every individual frame and provides a ARFrame object which contains a captured image, detailed tracking and camera position/orientation.

## Positioning/Feature Points
When you move the camera ARKit will gather a real-world tracking points. These points have a trackable feature within the real world and provides depth information like distance, position and orientation in the real-world coordinate system.

## Anchors
To place an object in the real world we need the real-world position that can be used for placing in an AR Scene. An anchor is a position and orientation in real-world space. ARKit will maintain that position and orientation for you as you move the camera around

## Lighting
ARKit uses the camera sensor to estimate the total amount of light available in a scene and applies the correct amount of lighting to virtual objects. It will make the object an integral part of the reality.



## Apps use ARKit?
It’s early days for ARKit. However, there are already lots of apps showing off what it can do.Few of the best are

1- Pokémon Go is probably the biggest game that uses ARKit right now.




2- The Machines is a multi-player RTS game that lets several people play in the same AR environment.




3- Skyguide is a very neat astronomy app that pastes constellations onto the sky




4- ModiFace 3D lets you see how you’d look with a different hair colour.




5- ARZombie is a classic example of an AR game. It puts you in a zombie home invasion scenario, 3D-modelled undead breaking in and attacking.




## Conclusion
ARKit with iOS opens up a lot of possibilities for developers to create innovative apps. The best thing about augmented/mixed reality is that it’s not limited to gaming — it can have applicability in real business cases. 
