#!/bin/bash

# gift [text] -n

# The text?
GIF_TEXT=$1
shift

# Default number of frames in the gif is set to 20
NR_OF_FRAMES=20

# Color of the text is set to black by default
TEXT_COLOR="black"

# 4:th argument is the background color
BG_COLOR="white"

# Start position of the text.
TEXT_POS=87

TEXT_END_POS=${#GIF_TEXT}

## echo $TEXT_END_POS

# Check flags 
while [ "$1" ]
do
	case $1 in
		-frames)
			shift
			NR_OF_FRAMES=$1
			#echo $NR_OF_FRAMES
		;;
		-text-color)
			shift
			TEXT_COLOR=$1
			#echo $TEXT_COLOR
		;;
		-help)
			echo "Welcome to the help page of gift. Sorry but i can't help you.."
			exit
		;;
		-background-color)
			shift
			BG_COLOR=$1
			#echo $BG_COLOR
		;;
		*)
			echo "What is this? --> $1" >&2
			exit 1
		;;
	esac
	shift
done

# Test that the number of frames is a positive integer
if ! [[ "$NR_OF_FRAMES" =~ ^[0-9]+$ ]]
	then
		echo "Illegal argument: $NR_OF_FRAMES" >&2
		exit 1
fi

if ! [[ "$TEXT_COLOR" =~ ^(white|black|red|green|blue|yellow|purple|orange|cyan|indigo|magenta|pink|brown|gray)$ ]]
	then 
		echo "Illegal argument: $TEXT_COLOR" >&2
		exit 1
fi

if ! [[ "$BG_COLOR" =~ ^(white|black|red|green|blue|yellow|purple|orange|cyan|indigo|magenta|pink|brown|gray|none)$ ]]
	then 
		echo "Illegal argument: $BG_COLOR" >&2
		exit 1
fi

# convert -size 127x127 xc:none -font "Arial" -pointsize 120 -fill $TEXT_COLOR -draw "text $TEXT_POS,95 \" $GIF_TEXT" shit.png