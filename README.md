# Smart Mirror

Google Assistant talking smart mirror; I created this project based upon ideas I had seen on the internet. This was a fun project to learn new skills. It is interactive through
the use of Google Assistant; the calendar on screen can be updated real time by voice and it can talk to you while you brush your hair.

## How it was made

The mirror consists of two-way glass, a Raspberry Pi, and a monitor. The entire frame was built from scratch by hand. The Raspberry Pi runs an image of Raspbian that allows for vocal recognition.
Using this image, a Google Assistant was created using the Google Cloud Platform. The Google Assistant runs on start-up through the `assistant_grpc_demo.service` script. Through personalization on Google 
account services, this assistant is setup to behave like other Google Assistant devices.

The Raspberry Pi also runs a mirror module to create a user interace that replicates a real mirror but with interactive features. This module does not run automatically on start-up but is 
controlled by `mm.sh`.

-- insert image here--

### Google Assistant

Using the [Google AIY Voice Kit](https://aiyprojects.withgoogle.com/voice-v1/), a Google Assistant module was created. 
The Google AIY Kit included a microphone and voice HAT board for vocal recognition. See the associated link for instructions on how to download and use the assistant.

### Magic Mirror Module

The open source [MagicMirror](https://github.com/MichMich/MagicMirror) module creates a mirror interface. `config.js` is the configuration that I created for my mirror; I display my calendar, the date, weather, and an dog graphic.
There are many other modules available to customize your mirror interface. See the associated link for instructions on how to download and use the module.

## Future Improvements

- Addition of lights to activate whenever Google speaks.
- Music playing capabilities; the current voice HAT only supports voice-over.
- Wall stand to allow for easy access.
- "Magic mirror on the wall..." command.
