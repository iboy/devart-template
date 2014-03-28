# Development Approach #

As the project has been underway for a while (it is part of my DPhil at the University of Sussex), the general developmental approach is 'iterative' and exploratory but with the broad goal of creating a performance animation system with flexible modes of embodied input, including: multitouch, multiuser, computer vision (Kinect), hand pose tracking (LeapMotion) and face and gaze tracking (using the Kinect and FaceShift)). With the exception of face input, I have all the others working in prototype form.

Some problems are standing some have been solved, but require improvement. For this phase of the project I have set the following design / developmental goals:

- create a scheme for jointed rigid body characters (to facilitate quick creation of animatable objects)
- explore methodologies for blending physics based animation with real-time interaction and traditional key framing (pre made animated sequences) - a hybrid real-time performance animation approach
	- in pursuit of this I wish to integrate IK / FK / FABRIK (Forward And Backward Reaching Inverse Kinematics) into the existing physics based model.
- integrate silhouette exploration and shadow oriented visual effects;
- implement a 'recorder' solution that will capture Open Sound Control (OSC) messaging and effectively record a performance. I know in theory how to accomplish this using existing OpenFrameworks tools (ofxTimeline, Duration) and Osculator. It would be nice to get a demo working; **UPDATE: Done!**
- explore methods to capture visitor silhouettes and incorporate them into the animated shadowgraph;
- optimise touch as input (this may not be configurable in an installation set up - dependent on equipment) - touch is - in my view - the most nuanced approach to controlling  this style of puppetry and if budgets allowed a multi-user larger touch surface or multiple tablets (if secured) could allow for touch input in a public space;
- Create a sane 'settings' environment for presets and OSC / network settings;  **UPDATE: Done!**

![Development Approach](../project_images/reading.png?raw=true "Developmental Approach")
