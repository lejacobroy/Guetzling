# Introduction

Guetzling is a simple script for macOS and Linux written in Bash to automate (recursively finding files) the compression of JPGs and PNGs using the Guetzli algorithm.

By design, Guetzling will overwrite and/or delete your original files.  If you want to keep your originals, make a backup of your folder before using Guetzling.

## Install Guetzli
1. Install [Guetzli](https://github.com/google/guetzli), via the directions provided at the link.
2. Copy Guetzling, copy it to `/usr/bin`.

## Usage
1. Simply `cd` to the parent directory of your choice, and `guetzling`. ***Voilà!***

## Adjustable Parameters

By Default, Guetzling uses the following options:
 
- JPGs are re-compressed and overwritten
- PNGs are converted to JPG and the originals are deleted
- Quality Level is for Guetzli is set to 95

You can adjust these options using bash arguments:

1. Quality for JPG re-compression.
	- Requires a value between 84 and 100 for Guetzli is designed to fail
	- Default value is the same as Guetzli: 95
 
 2. Quality for PNG conversion.
	- Requires a value between 84 and 100 for Guetzli is designed to fail
	- Default value is the same as Guetzli: 95
	
3.  Compress JPGs
	- Set to "false" and Guetzliing will ignore JPG/JPEG files, compressing only PNGS.
	
4. Compress PNGs
	- Set to "false" and Guetzling will ignore PNG files, compressing only JPGS
 
 5.  Delete PNG
 	- Set to "false" and Guetzling will keep the copy of any original PNGs in your folder
 

## Example Usage
 
 Replace all files at quality 95:
 
 	./guetzling
 	
 Convert JPGs at 95, PNGs at 84, and keep your original PNG files:
 
 	./guetzling 95 84 true true false
 	
 Convert only JPGs at Quality Level 97:

	./guetzling 97 95 true false
  	 