# Project-Bumper-Brawl

NOTE: We couldn't get the game to build and didn't have time to sort out the error. The screenshot of the error we got is included.

AJ Bwejesa - Programmer/making charts
Donovan Mills - Programmer/making charts

50/50

AJ's github account will be seen as uploading most of the work as he is the one who performed the copy-paste from our GDW repo to this repo to start.

We are using our GDW project Bumper Brawl, a party game where players controlling cars will brawl in a sumo-style to push each other out of safe zones which decrease in size and change location every 30 seconds to score points.

Singleton: We implemented a basic player controller/input manager Blueprint as a singleton because being able to control the player and expand upon our controls' functionality as we go will be important for adding things like controller support for eventual local multiplayer. We also implemented a timer manager via an actor component Blueprint with a UI element as our second singleton, which is going to be very necessary to communicate to the player how much time is left before the safe zone changes and begins the next cycle.

Factory: We will be using Factory design to create procedural obstacles. We will have a parent Blueprint spawn obstacles with a child wall and ramp factory to spawn different types of obstacles. This will bring variability to the game so that it is not inherently solvable. Our safezones will also be handled by a factory so that we can easily vary their size and position to once again add more randomness so that each round of the game will be unique.

Command: We will be using Command to manage custom button mapping which will be particularly important for when multiplayer is eventually added so that players can customize both controller controls and keyboard/mouse controls as they please by using a Blueprint to execute different custom functions. Our second command pattern will be our camera control, so that we can switch between different game cameras based on what is happening in the game.

Observer: Our main boundary will be implemented with observer so that we can trigger events like sounds and update the UI when the player approaches a boundary, amongst other things. We will also be using observer to monitor the cars' health to trigger events based on health changes, like playing effects on death which will add fun/juice to our game.
