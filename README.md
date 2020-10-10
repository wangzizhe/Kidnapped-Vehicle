# Overview
Project 6: Kidnapped Vehicle of Udacity's Self-Driving Car Nanodegree.

## Project Introduction
The robot has been kidnapped and transported to a new location! Luckily it has a map of this location, a (noisy) GPS estimate of its initial location, and lots of (noisy) sensor and control data.

In this project a 2 dimensional particle filter will be implemented in C++. A simulator is provided by Udacity. The particle filter will be given a map and some initial localization information (analogous to what a GPS would provide). At each time step the filter will also get observation and control data.

The job is to build out the methods in `particle_filter.cpp` until the simulator output says:

```
Success! Your particle filter passed!
```

![img](.\success.png)

Here is a video of this project.

[![](http://img.youtube.com/vi/0ehog2oVSjQ/0.jpg)](http://www.youtube.com/watch?v=0ehog2oVSjQ "Kidnapped Vehicle")

## Running the Code

Following commands are used to clean, compile and run the codes.

```
./clean.sh
./build.sh
./run.sh
```

Then a message will be shown to indicate the filter is listening:

```
Listening to port 4567
```

## Inputs to the Particle Filter
The inputs to the particle filter can be found in the `data` directory.

#### The Map*
`map_data.txt` includes the position of landmarks (in meters) on an arbitrary Cartesian coordinate system. Each row has three columns
1. x position
2. y position
3. landmark id

### All other data the simulator provides, such as observations and controls.

> * Map data provided by 3D Mapping Solutions GmbH.

## Success Criteria
the things the grading code is looking for are:
1. **Accuracy**: the particle filter should localize vehicle position and yaw to within the values specified in the `parameters max_translation_error` and `max_yaw_error` in `src/main.cpp`.
2. **Performance**: the particle filter should complete execution within the time of 100 seconds. 