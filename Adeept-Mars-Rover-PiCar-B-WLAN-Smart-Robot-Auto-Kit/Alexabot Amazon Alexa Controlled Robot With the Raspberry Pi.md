### Alexabot: Amazon Alexa Controlled Robot With the Raspberry Pi

https://www.dexterindustries.com/projects/alexabot-amazon-alexa-controlled-robot/

NOTE: This tutorial is outdated. Please refer to Alexa Voice Service  SDK 

In this tutorial we build Alexabot, the Amazon Alexa Controlled Robot, using the Raspberry Pi.  We will walk you through the steps of building a voice controlled robot with the Raspberry Pi and GoPiGo.  With Alexabot, you can command the Raspberry Pi Robot around with commands like “Alexa Forward!” or “Alexa Coffee!”.

Finally, a Raspberry Pi Robot to answer your bidding, with only the sound of your voice!

Overview of the Amazon Alexa Controlled Robot

Amazon Alexa software can be put on the Raspberry Pi Robot, the GoPiGo.  In this project, we wanted to create an Alexa-based robot that would respond to voice commands, as well as answer your questions.  You can ask Alexabot “How hot is it in Dubai?”  or “What’s the weather like in London?”.  What makes Alexabot really interesting is that you can command it around with your voice, using the Alexa Voice Service.

With Alexabot you can command the Raspberry Pi robot around with commands like “Alexa Forward!” or “Alexa Coffee!”.

Amazon Alexa Controlled Robot Hardware SetupHardware Set Up
The hardware set up to build the Alexa controlled robot is very simple.  We used the following parts:

The GoPiGo – The body of the robot.  The GoPiGo is going to do Alexa’s bidding.
The Raspberry Pi 3 – The brains of the operation. Using the Pi3 version of the Raspberry Pi board is very helpful in speeding up the operation due to its faster chip. AlexaPi is somewhat demanding, to be polite.
Raspbian for Robots – Most of the software for this project is pre-installed.
The Speaker for the Raspberry Pi – Alexabot will talk back to us, so we’ll need a speaker to hear her voice.
A USB Microphone – Our way to talk to Alexabot.  This one is plug and play and seems to work well in a noisy room.
Set up is quick and easy.  First step is to assemble the GoPiGo Robot for the Raspberry Pi.  Then we mounted the microphone to one of the USB ports in front of the GoPiGo.  Finally we mounted the speaker for the Raspberry Pi to the top of the GoPiGo and held it in place with a ziptie.  The robot is powered with 8XAA batteries.

Software Set Up
Alexabot works by using a few services strung together.

AlexaPi: First, we use Alexa Voice Services to listen for commands, using the AlexaPi project software.
IFTT: This passes the data to If This Then That.
ngrok: We connect back to the Pi using the ngrok service.
Flask: Finally, we listen for commands, and control the robot using a python program using a very simple Flask server.
alexabot-schematic Amazon Alexa Controlled Robot Schematic 

 Click the (+) below to see the details of each step.
Setting Up AlexaPi
Setting Up IFTTT
Connect to ngrok
Set Up the Flask Server
Alexabot is an amazon alexa controlled robot that moves when you command it.
Your wish is my command.

Running the Amazon Alexa Controlled Robot
Now, with all the services set up, we should be able to say a command like “Alexa trigger forward”, Alexa will alert IFTT, which will send an HTTP message through ngrok back to our GoPiGo and post to the web server running in Flask.  The Flask program will command the GoPiGo to move forward.

The quickstart to get running with Alexabot are to first start AlexaPi:

sudo python /opt/AlexaPi/src/main.py
Next, start ngrok in a separate window:

sudo ~/ngrok/ngrok http -subdomain=dexterindustries -log=stdout 5000 > log.txt &
Finally, start the Flask server:

sudo python alexabot-flask-app.py
Start talking!  Remember your commands need to start with “Alexa trigger . . . ” and then the command you want to robot to do.

Moving Our Amazon Alexa Controlled Robot Forward
One area of improvement in our Amazon Alexa Controlled Robot might be to reduce lag.  With a steady internet connection, I left Alexabot running all weekend and it was still responsive in the morning (update: 5 days and counting).  However, you’ll notice there is a varying amount of lag between commands and response.  There are so many services strung together some slowdown is likely.  The next step and future improvement would be to develop our own service on Alexa to return the text command directly.

Want to build it yourself?  You can get the GoPiGo and Raspberry Pi here!  We would love to hear if you build your own Amazon Alexa controlled robot!