# bad-console
Bad Apple for the developer tools console. Tested on Chrome, Edge and Firefox, using Windows.

I'm using SVG files solely to get Firefox to render the frames, the Firefox console has a 8Kb log limit (unlike Chrome and Edge), this causes Firefox to drop the occasional frame as they are too large. Firefox also has a flickering effect, so I've added a warning for visitors to be careful of that.

I update frames with a 30fps animation loop, although the animation may lag at parts it should be quite robust at staying in sync. Firefox can't seem to play the video when I want it to, so I get Firefox browsers to skip ahead a bit in the video to try and sync up again.

Frames where taken from the source video using ffmpeg,
converted to svg with Potrace,
then the SVG was converted to Base64 encoded image with JavaScript btoa().

The drawing to the console function is adapted from defaced.dev's code, 
https://defaced.dev/tools/consoleimg/
