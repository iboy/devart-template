# Project Title
The ShadowEngine: A Tool for Digital Puppetry and Collaborative Co-Creation

## Authors
- Ian Grant, [iboy](https://github.com/iboy "iboy on github") on github

## Description
The ShadowEngine is the latest iteration of a digital puppetry system, enabling real-time character, cinematic and scenographic control over a shadow theatre simulation. The primary aim is to create a performance animation system where live collaborative co-creation of expressive movement and story-making takes place. It can be present in a number of different configurations: as an installation, a performance or a workshop experience.
### Kinetic Objects and Expressive Movement
I am motivated by a fascination with animation: especially interactive, kinetic and expressive performing objects (puppets). Game-engines and creative coding platforms facilitate novel means to explore multiple dimensions of real-time animation, including:  soft and rigid body physics, spring systems, collisions, blended animation, the use of physical controllers and other sensors to create virtual and physical movement.

Current control experiments include multiple Kinect and Leap Motion control, multiple touch controllers (iOS or Android), eye-tracking (exploring accessible control techniques for complex animation) allowing as many people as devices and the WIFI / OSC network allows to simultaneous perform with virtual objects and direct the live animation. 

Iterations include work in a variety of creative coding environments: Quartz Composer, OpenFrameworks and Animata , playing with physics libraries like Bullet, Box2D and computer vision libraries (OpenCV). In the latest Unity prototype I've experimented incorporating generative environments into the shadowgraphs -- including other open source creative coding experiments --  more of that in the blog. 

The latest iteration includes archival shadow puppets (Karagöz) scanned at a research residency at the Institut de la Marionnette, Charleville, France. But any kind of shadows can be explored in homage to forgotten shadow performance e.g. Le Chat Noir, Lotte Reiniger's silhouette films or the abstract shadow objects play of Herta Schonewölf.

## Link to Prototype
NOTE: If your project lives online you can add one or more links here. Make sure you have a stable version of your project running before linking it.

[Example Link](http://www.google.com "Example Link")

## Example Code

The code below sets the default state of a multi touch controller interface (like an iPad or an android device) using OSC.

	void Start() {
		
		
		/* SET DEFAULTS ON OSC INTERFACE  THIS SHOULD BE REFACTORED INTO A CONTROLLER*/
		// create a transmitter to sync the UI
		
		transmitter = new OSCTransmitter(SendToIPAddress, port);
		transmitter.Connect();
		connected = true;
		//myMessage = new OSCMessage("/4" ); // switch to the fourth tab in TouchOSC
		//transmitter.Send(myMessage);
		myMessage = new OSCMessage("/3/CameraZoomOrtho", 2.61f ); // switch to the fourth tab in TouchOSC
		transmitter.Send(myMessage);
		myMessage = new OSCMessage("/3/FXSunShaftsIntensity", 4.0f ); // switch to the fourth tab in TouchOSC
		transmitter.Send(myMessage);
		myMessage = new OSCMessage("/3/FXVignetteSize", 5.08f ); 
		transmitter.Send(myMessage);
		myMessage = new OSCMessage("/3/FXVignetteBlur", 1.0f ); 
		transmitter.Send(myMessage);
		myMessage = new OSCMessage("/3/FXVignetteChromatic", 1.98f ); 
		transmitter.Send(myMessage);
		myMessage = new OSCMessage("/3/DOFToggle", 0 ); 
		transmitter.Send(myMessage);
		myMessage = new OSCMessage("/3/CameraTypeToggle/1/2", 0 ); 
		transmitter.Send(myMessage);
		myMessage = new OSCMessage("/3/FXMotionBlur", motionBlurAmount ); 
		transmitter.Send(myMessage);

		myMessage = new OSCMessage("/3/IrisLocationXYPad/x", 0.0f);
		transmitter.Send(myMessage);
		myMessage = new OSCMessage("/3/IrisLocationXYPad/y", 0.0f);
		transmitter.Send(myMessage);

		myMessage = new OSCMessage("/3/IrisTransitionSpeed", 0.2f);
		transmitter.Send(myMessage);
		irisDiameter(.2f);

		myMessage = new OSCMessage("/3/ManualFadeSlider/x", 0.0f);
		transmitter.Send(myMessage);
		// set all object scales to 1

		// init captions list
		initCaptionList();


## Links to External Libraries
 
[Soulwire's Recursion Toy](http://soulwire.co.uk/data/experiments/recursion-toy/ "Soulwires Recursion Toy")
[Soulwires Recursion Toy on GitHub](https://github.com/soulwire/Recursion-Toy "Soulwires Recursion Toy on GitHub")

TODO
Assets; OSC.net; Unity OSC;
## Images & Videos
NOTE: For additional images you can either use a relative link to an image on this repo or an absolute link to an externally hosted image.

![Example Image](project_images/cover.jpg?raw=true "Example Image")

https://www.youtube.com/watch?v=30yGOxJJ2PQ
