# Gaze-Tracking
**Purpose:** To inspire creativity in others to find meaningful applications for gaze tracking.

**Summary:** A conglomeration of AR experiences that showcase the power of gaze tracking. The experiences herein can be classified into two primary groups,  proofs of concept or analytical applications. Each experience highlights a separate use case and is intended to inspire creators think about how gaze tracking could enhance their own AR experiences.

### **Table of Contents**

- [What is Gaze Tracking?](#what-is-gaze-tracking)
- [Model Manipulation](#model-manipulation)
  - [Basic Model Manipulation Demo](#basic-model-manipulation-demo)
  - [Timing Gaze Duration Demo](#timing-gaze-duration-demo)
  - [Put That, There Demo](#put-that,there-demo)
- [Analytical Applications](#analytical-applications)
  - [Ring of Colored Labels](#ring-of-colored-labels)
  - [Field of Colored Labels](#field-of-colored-labels)
  - [Board of Colored Labels](#board-of-colored-labels)

## What is Gaze Tracking?

### Background Explanation

Before we jump right into an explanation of gaze tracking, it is important that you understand a little bit about how the position and orientation of objects are defined in a virtual 3D space. To start off, virtually positioning an object in a 3D environment isn't something that was invented for augmented reality. It has actually been around much longer and is widely used in almost every video game you have ever played. It is what allows the computer to keep track of your character and the other objects in the environment and is crucial as you move throughout the virtual area.

In order to define an object's position, the computer must know the object's location and which way it is facing. The location data typically come in the form of 3-dimensional coordinates *(X,Y,Z)*, while the orientation data are commonly a set of angles or orthogonal vectors. These data fully-define any object in 3D space and are essential for a realistic rendering of the virtual environment.

### Position & Orientation in Vuforia 

Vuforia Engine defines objects within the augmented reality space using these same principles. Every object that is placed into the AR experience must have both its position and orientation defined. With this definition, the AR exprience is rendered consistently, no matter where the user is viewing from. Every widget (e.g., model, model item, 3D label) can be given X,Y,Z-coordinates, as well as X,Y,Z-rotations.

The user's position and orientation are also defined out of necessity and are constantly changing as they move through the AR space. These definitions are always made to track the user's device, whether it be a mobile device, or an AR headset. In contrast to the angles used for the other objects in the experience, the user's orientation is defined by a pair of orthogonal vectors. In the image below, the user's 3D coordinates relative to the experience origin are represented by the yellow point. The blue vector is normal to the user's device screen and represents the direction in which they are looking. The green vector is orthogonal to the blue and points vertically out of the device. It tells how the user's device is rotated about the blue vector and defines the remaining critical information.

<img src="images/User%20Position%20%26%20Orientation.PNG" width="450">

By figuring out how to access this complete set of data, we could know exactly where the user is and where they are looking in realtion to the objects in the AR experience. This knowledge would allow us to take our AR experiences to the next level by using the user's position and gaze to find out more about what they are actually seeing. We can use these data to manipulate the objects in the experience or perform analysis and learn more about the users.

## Model Manipulation

In order to show some 
