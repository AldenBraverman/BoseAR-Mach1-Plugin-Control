# BoseAR Mach1 Plugin Control

One challenge I approached as an audio mixing engineer is finding accessible tools for mixing ambisonic/spatial audio. [Mach1](https://www.mach1.tech/) has built excellent [VST plugins](https://www.mach1.tech/downloads) to spatialize audio signals, I wanted to build on their monitoring tools. Mach1 has a [mobile app](https://apps.apple.com/us/app/m1-mntr-ctrl/id1486961476?ls=1) that acts as an [OSC](http://opensoundcontrol.org/introduction-osc) bridge between their monitoring plugin and [BoseAR hardware](https://www.bose.com/en_us/better_with_bose/augmented_reality.html), however this prevents audio monitoring through the BoseAR hardware without advanced audio routing. I was unable to find a desktop tool that allows me to control the monitor VST with BoseAR hardware, my goal was to build a tool that would enable an audio engineer to do this. This tool enables real-time spacial audio monitoring with BoseAR hardware.

## Getting Started

Clone this repo and install the prerequisities.

### Prerequisites

You will need Unity version 2019.3.0f6 to act as the OSC bridge. This can be downloaded and used for free, make sure to install the Unity Hub first before downloading the verison.
* [Unity](https://unity3d.com/get-unity/download)
* [Version 2019.3.0](https://unity3d.com/get-unity/download/archive)

You will need a digital audio workstation to set up the audio monitoring environment. Reaper is an excellent choice and it's evalution license can be used for free.
* [Reaper](https://www.reaper.fm/)

BoseAR hardware utilizes Mach1 for audio spatialization. You will need Mach1's plugins that will encode and decode the spatialized audio signals. You can request a 3-month trial license for free; It is worth noting that I requested my trial license during the COVID-19 outbreak and that the trial license terms could be changed in the future.
* [Mach1 Spatial System](https://www.mach1.tech/downloads)
* [Mach1 Trial License](https://www.mach1.tech/trial)


### Installing

Follow the installation instructions for each prerequisite, they should be fairly simple. Add the project folder in this repo to Unity Hub and make sure the project can open without errors. 

## Running the tests

Open the Unity project and the Mach1 Spacial Template (Mach1 Spacial Template.RPP). On the monitor bus in Reaper, expose the M1-Monitor plugin parameters and make sure that the plugin is using the port 9898 for OSC messages. Connect your BoseAR hardware via USB to your computer and play the Unity scene. Unity will then identify your hardware and start sending OSC messages to the plugin. In Reaper, switch your audio output device to your BoseAR hardware to monitor directly through the hardware.

## Built With

* [Unity](https://unity3d.com/get-unity/download) - Application Framework
* [BoseAR Unity SDK](https://developer.bose.com/bose-ar/unity) - Manages BoseAR interfacing
* [OSC Simpl](https://assetstore.unity.com/packages/tools/input-management/osc-simpl-53710) - Used to create and send OSC messages

## Contributing

Please reach out to me directly - abraverm@terpmail.umd.edu

## Authors

* **Alden Braverman** - [LinkedIn](https://www.linkedin.com/in/alden-braverman-87ba48126/)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Special thanks to [MAVRIC](https://mavric.umd.edu/), [Lucien B Parsons](https://www.linkedin.com/in/lucienp/), [Sammy Popat](https://www.linkedin.com/in/sameerpopat/) and the [Innovation Gateway](https://innovate.umd.edu/) for providing me with BoseAR hardware.
* Thanks to Amanda Whitt, Art Gibson and Gabriel Butterick at Bose

