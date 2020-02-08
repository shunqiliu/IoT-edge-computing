# CLI on SAM W25.
This project is the implementation of CLI on SAM W25, compiled by Atmel Studio 7.0, running on Windows 10. User should use teraterm,
or similar serial communication software to test the project.
## commands for CLI
### help
#### Description
Prints all the available commands and a short synopsis

#### Inputs
None

#### Output
List of all available commands and their descriptions
### ver_bl
####Description
Prints the bootloader firmware version

#### Inputs
None

#### Outputs
String in the format MAJOR.MINOR.PATCH

#### Notes

a. i.Use MAJOR.MINOR.PATCH versioning, per https://semver.org/

b. ii.Store each number as an unsigned 8-bit integer

c. iii.Example output: 1.4.88, where MAJOR = 1, MINOR = 4, PATCH = 88

For this homework: Print any static number.
### ver_app
#### Description
Prints the application code firmware version

#### Inputs
None

#### Outputs
String in the format MAJOR.MINOR.PATCH

#### Notes:

Use MAJOR.MINOR.PATCH versioning, per https://semver.org/

i.Store each number as an unsigned 8-bit integer

ii.Example output: 1.4.88, where MAJOR = 1, MINOR = 4, PATCH = 88

For this homework: Print any static number.
### mac
#### Description
returns the mac address of the device

#### Inputs
None

#### Outputs
mac address in standard form ff.ff.ff.ff.ff.ff, where each octet is in hex.

#### Notes
The mac address resides with the ATWINC chip so you will need to query it. e. Example: f.

This function only needs to return dummy info for now.
### ip
#### Description
returns the ip address of the device in the standard format: ex. 255.255.255.255

#### Inputs
None

#### Outputs
current IP assigned to the device.

#### Notes
The IP address resides with the ATWINC chip so you will need to query it for the address.

This function only needs to return dummy info for now. You can return 255.255.255.255 always
### devName
#### Description
Returns the name of the developer (your name)

#### Inputs
None

#### Outputs
Your name, in ASCII, or nickname

Notes: k. This function only needs to return dummy info for now.
### setDeviceName <string name>

#### Description
Sets the name of the device to the given string

#### Inputs
A string (separater from “setDeviceName” by a space

#### Output
“Device name set to <string name>”

Example: setDeviceName ROOM1DEVICE

For now we can save this in volatile memory (ram).
### getDeviceName
#### Description
Gets the name of the device to the given string

#### Inputs
None

#### Output
“Device name is ‘<Device’s name>”

Example:

getDeviceName

<<Device name is ROOM1DEVICE

## Files
Other libraries should download from Atmel Studio 7
### asf.h
Library for SAM xxx microcontroller
### main.c
Main running code
### circular_buffer.c/.h
Implementation of ring buffer
### SerialConsole.c/.h
Implementation of CLI functions. (Also includes other important UART code)

## Statement
This project is a part of University of Pennsylvania, only SerialConsole.c is worked by author, and other files are designed by courses.
