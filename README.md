# Introduction

Guetzling is a simple script for macOS and Linux written in Bash to automate (recursively finding files) the compression of JPGs and PNGs using the Guetzli algorithm.

By design, Guetzling will overwrite and/or delete your original files.  If you want to keep your originals, make a backup of your folder before using Guetzling.

## Install Guetzli
1. Install [Guetzli](https://github.com/google/guetzli), via the directions provided at the link.
2. Copy Guetzling, copy it to `/usr/bin`.

## Usage
1. Simply `cd` to the parent directory of your choice, and `guetzling`. ***Voilà!***

## Adjustable Options

By opening the script in a text editor, you can adjust certain variables to change the output of Guetzling.

### JPG

Enable/Disable re-compression of JPG and JPEG files using Guetzling.

	#Recompress JPG Images
	#Set to false to disable
	JPG=true

### PNG

Enable/Disable the conversion of PNG to JPG using Guetzling.

	#Convert PNG Images
	#Set to false to disable
	#PNGS WILL BE DELETED AFTER CONVERSION
	PNG=true

### QUALITY

Change Guetzling/Guetzli Quality Level.

	#Set Quality level
	#Default = 95
	#Max = 100
	#Min = 84
	QUALITY=95