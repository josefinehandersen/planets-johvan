# Background
Theory: The gravity from the other planets, especially Jupiter, causes the change of the eccentricity.

Problem: Reproduce Milankovitch cycle of eccentricity (100ka)

Method: Use Python

Input: Some initial positions of the planets but no external data

Output: Graph of orbits and a timeseries of an eccentricity parameter

**Development steps**

-   Earth-sun system

-  Add Jupiter

-  Make modular


# Planet flowchart
```uml
@startuml
skin rose
title Planet flowchart
start

:define some parameters;
:initialize earth (and Jupiter);

repeat
  :calculate new position;
  :calculate acceleration;
  :calculate velocity in two dimensions;

repeat while (simulation time is met) is (no)
->yes;
:figure plotting;
stop
```

# Pseudo code
```code
Define constants
Define initial values
	positions
	velocity (balance of gravity and centrifugal force)
(Allocate (book) space for long vectors	plan iteration)
Iteration
	Change of positions
	Calc acc (gravity)
	Calc new velocity
Plot resulting ellipses
Calculate orbit parameters
Plot time series of parameter change
```
