# bad-console
Bad Apple for the developer tools console. Tested on Chrome, Edge and Firefox, using Windows.

Go to https://jhancock532.github.io/bad-console/, and wait for the video data to load. 

Note that this site costs 43MB of data, 21MB of SVG frames and 22MB of mp4 video. A WebM would be nicer.

I'm using simplified SVG files to get Firefox to render the frames, as the Firefox console has a 8Kb background image limit (unlike Chrome and Edge). This causes Firefox to drop the occasional frame as they are too large. Firefox also has a flickering effect, so I've added a warning for visitors to be careful of that.

I update frames with a 30fps animation loop, although the animation may lag at parts it should be quite robust at staying in sync. Firefox can't seem to play the video when I want it to, so I get Firefox browsers to skip ahead a bit in the video to try and sync up again.

Frames where taken from the source video using ffmpeg,
converted to SVG with Potrace,
then the SVG was converted to Base64 encoded image with JavaScript btoa().

The drawing to the console function is adapted from defaced.dev's code, 
https://defaced.dev/tools/consoleimg/

Shoutout to [the original Bad Apple Browser Console repository](https://github.com/g-otn/bad-apple-browser-console), that logged Bad Apple using braille characters.
