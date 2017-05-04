# Introduction

Guetzling is a simple script for macOS and Linux written in Bash to automate (recursively finding files) the compression of JPGs and PNGs using the Guetzli algorithm.

By design, Guetzling will overwrite and/or delete your original files.  If you want to keep your originals, make a backup of your folder before using Guetzling.

## macOS Install
1. With Homebrew :
 `brew tap lejacobroy/homebrew-guetzling`
 
 And then,
 
 `brew install guetzling`.

## Linux Install
1. Install [Guetzli](https://github.com/google/guetzli), via the directions provided at the link.
2. Copy Guetzling to `/usr/bin`.

## Usage
1. Simply `cd` to the parent directory of your choice, and `guetzling`. ***Voilà!***

## Adjustable Parameters

By Default, Guetzling uses the following options:
 
- JPGs are re-compressed and overwritten
- PNGs are converted to JPG, re-compressed, and the originals are deleted
- Quality Level is set to 95

You can adjust these options using flags:

`-q` Quality for JPG or PNG re-compression.
	- Requires a value between 84 and 100.
	- Default value is the same as Guetzli: 95.
	
`-j` Compress JPGs ONLY
	- Use this flag and Guetzling will ignore PNGs files, compressing only JPGs.
	
`-p` Compress PNGs ONLY
	- Use this flag and Guetzling will ignore JPGs files, compressing only PNGs.
 
`-k` Keep PNG
 	- Use this flag and Guetzling will keep original PNGs files, and output compressed JPGs.
 

## Example Usage
 
 Replace all files at quality 95 :
 
 	`./guetzling`
 	
 Convert PNGs at 84, and keep your original PNG files :
 
 	`./guetzling -q 84 -p -k`
 	
 Convert only JPGs at Quality 97 in /Users/test/photos/output :

	`./guetzling -q 97 -j -f /Users/test/photos/output`
  	 