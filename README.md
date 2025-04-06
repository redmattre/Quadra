# Quadra

Quadra is a plugin that converts polar coordinates into cartesian coordinates.

![Quadra in action in reaper](/media/quadra1.gif)

## How it works

The following example shows how Quadra can be used to convert ambisonic polar coordinates (azimuth and elevation) into 2D cartesian coordinates for use with the d&b Soundscape object-based spatialization system.

1. The IEM Stereo Encoder plugin generates ambisonic automation.
2. Quadra converts polar coordinates into cartesian coordinates (you can either copy the ambisonc automations or link the azimuth and elevation of your ambisonic plugin).
3. Quadra sends out X and Y positions as 14-bit MIDI CC messages that can be routed to another plugin parameter.
4. In this case the d&b Soundscape plugin receives the data and controls the spatial position of the sound.

Note: in the release download you'll find a REAPER project file that shows the principle.  
Of course you'll need to download the [IEM Stereo Encoder plugin](https://plugins.iem.at/) and also the [d&b Soundscape plugin](https://github.com/dbaudio-soundscape/db-Soundscape-DAW-Plugins).  
These are all free plugins.

## Coordinate conversion

The mathematical logic behind Quadra is based on projecting a point on a sphere (defined by an azimuth and a perimeter angle) onto a 2D square.  
Imagine looking at the sphere from above: the higher the elevation (azimuth), the closer the point moves toward the center.  
At the edges (lower elevation), the projection follows the shape of a square.  
At the center (higher elevation), the shape becomes more circular.

This projection ensures a smooth transition from a square-shaped outer space to a circular center — like flattening an egg-shaped dome onto a square plane.

![3D simulation](/media/uovarino.jpeg)

## MIDI Routing

- X: CC 1-33  
- Y: CC 2-34

note: Quadra sends MIDI output that must be routed to the d&b Soundscape plugin. In this beta version the CC values are hardcoded.

## Notes

This project was developed as part of a PhD program, in collaboration with Tempo Reale, for use during the Bright Festival in Florence. It was designed to translate ambisonic-encoded versions of selected compositions by Luciano Berio for playback through the d&b Soundscape system.

This project consists of an RNBO patcher.