# Perfalyzer for ReShade

ReShade makes it WAY easy to intercept drawing API calls (if not specifically, at least generally) and so this project
aims to be an add-on for it which helps me to record metrics on various games so I can try to understand what's going
slowly or if things are being done in a stupid order, etc.

## How to Build

Prerequisites:
* Visual Studio (something relatively recent?)
* CMake

Should just work via CMake. I use CLion, but any CMake generator should work as well.

Make sure you check the architecture of whatever program you're trying to analyze, because 32-bit and 64-bit determines
whether ReShade will be able to load the add-on.

## Installation

* Requires the unsigned version of ReShade (I assume?)

Build the project, the copy the resulting DLL into the same directory as the executable where ReShade got installed, and
change the file extension from `.dll` to `.addon`.