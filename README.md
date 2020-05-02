[![Build Status](https://travis-ci.org/centic9/headset-charge-indicator.svg)](https://travis-ci.org/centic9/headset-charge-indicator)
[![Tag](https://img.shields.io/github/tag/centic9/headset-charge-indicator.svg)](https://github.com/centic9/headset-charge-indicator/tags)

A simple app-indicator for GNOME desktops to provide support for some wireless headsets.

Currently it supports displaying the battery charge and the 'chat-mix' level of Steelseries Arctis 
headphones. It also supports adjusting the mount of sidetone of the microphone.

It uses the tool from https://github.com/Sapd/HeadsetControl/ for connecting to a number of
popular headsets and fetches information to display it in the app-indicator bar
on the desktop.

## Installation

On Ubuntu/Debian based distributions, install the following packages

    sudo apt-get install python3-gi libappindicator3-1 gnome-icon-theme

On others, you might need to install `pygobject`, but this is untested, PRs with more information welcome!

### Building HeadsetControl

Follow the instructions at https://github.com/Sapd/HeadsetControl/ for building the binary and
note down the path to it.

You can test the helper application manually via `headsetcontrol -b -c`, this should print the current
battery level to the console.

## Usage

Build/install according to the instructions above then start it via 

    python3 headset-charge-indicator.py <location of headsetcontrol>

A Headset-icon should appear in the area for app-indicators together with a percentage number.

## Supported Headsets

Look at the description of https://github.com/Sapd/HeadsetControl/, headset which support 
at least fetching battery information are supported here as well, other functionality will work 
if the headset supports it.

## Licensing

* headset-charge-indicator is licensed under the [BSD 2-Clause License].

[BSD 2-Clause License]: https://opensource.org/licenses/bsd-license.php

## Like it?

If you like my software please star the repository.
