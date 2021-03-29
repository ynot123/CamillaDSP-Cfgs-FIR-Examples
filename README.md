# CamillaDSP Configurations and FIR-Examples
## Example Filter Configuration and Convolver Coefficients

This hub contains some example filter and convolver configurations for use with the excellent Camilla DSP program.

My basic system is made up of a Raspberry PI3 with an IQAudio DAC+ top hat piped into an soundbar and sub.  I found sound quality of the soundbar and sub to be lacking somewhat particularly as it pertains to music and thought it needed some help at both the top and bottom ends.  Tried some equalizer type apps but found the overall experience lacking somewhat. To that end, I put together this little project, now that soundbar sounds awesome (to my ears at least). 

### Software:
The system is a mash up of the following:
  - Debian Buster lite for the PI3 - the OS
    - https://www.raspberrypi.org/software/operating-systems/#third-party-software  - Raspberry Pi OS Lite
  - Camilla DSP - the DSP engine c/w web page gui and plotting library  
    - https://github.com/HEnquist/camilladsp  - Flexible linux IIR and FIR engine for crossovers, room correction, etc
    - https://github.com/HEnquist/pycamilladsp  - Python library for handling the communication with CamillaDSP via a websocket
    - https://github.com/HEnquist/camillagui  - Web based graphical interface to CamillaDSP
    - https://github.com/HEnquist/camillagui-backend  - Backend server for camillagui
    - https://github.com/HEnquist/pycamilladsp-plot  - Plotting tools for CamillaDSP
  - Squeezelite - the audio player of choice for my integrated home system 
    - https://github.com/ralph-irving/squeezelite  - Lightweight headless squeezebox player for Logitech Media Server
    - https://sourceforge.net/projects/lmsclients/files/squeezelite/  - Compiled binaries for all operating systems
    - https://ralph-irving.github.io/squeezelite.html  - Man page for squeezelite 
  - Audacity - free, open source, cross-platform audio software
    - https://www.audacityteam.org/  - Audacity is an easy-to-use, multi-track audio editor and recorder 

In the future, I may provide an image of my existing setup for common use but I feel the need to check on licensing, etc to see if that kind of thing is allowed first.  In the short term, I will provide some links to the software used and basic instructions on the setup if people are interested.

In this repository you will find:
#### Filter Configurations Directory (configs):
  -   Contains sample Camilla DSP configurations which include settings for sample rate, capture and playback devices, filter settings including gain, convolver, delay, biquad, etc, details for mixers and finally the pipeline details.
#### Convolver Coefficients Directory (coeffs):
  -   Contains several FIR coefficient files for use with the integrated convolver filter in Camilla DSP.  Most of these sample files have been derived from impulse files wich are commonly used with Viper4Android application.  These files can produce all kinds of effects and can alter the sound dramatically.  Be careful with their use and check the overall gain of the effect (or keep your volume low) before applying them.
  -   See Building_FIR.md document for a short how to.  The document outlines a fairly simple way to convert typical IRS wav files into FIR coefficient files. ## to do
#### System Configurations Directory:
  -   Contains several configration files required to integrate the various pieces of software, some scripts to help automate the startup, set initial filters, etc..
  -   See Install.md for a brief primer regarding building this project from the OS install, CamillaDSP installation and finally squeezelite player.  ## to do

More to follow as I get a bit of time to play and post.
