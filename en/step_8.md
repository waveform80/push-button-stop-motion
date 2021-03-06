## Generate the video

--- task ---

To generate the video, begin by returning to the terminal window.

--- /task ---

--- task ---

Run the video rendering command:

```bash
avconv -r 10 -i animation/frame%03d.jpg -qscale 2 animation.h264
```

*Note you're using `%03d` again - this is a common format which both Python and `avconv` understand, and means the photos will be passed in to the video in order.*

--- collapse ---

---
title: "avconv: command not found ?"
---

If you receive the error `avconv: command not found` you will need to to install `libav-tools`.

Enter the following commands in to the terminal to update and upgrade your system:

```bash
sudo apt-get update
sudo apt-get upgrade
```

Now install the `libav-tools` package:

```bash
sudo apt-get install libav-tools
```

--- /collapse ---


--- /task ---

--- task ---

Play your video using `omxplayer`.

```bash
omxplayer animation.h264
```

--- /task ---

You can adjust the frame rate by editing the rendering command. Try changing `-r 10` (10 frames per second) to another number.

You can also change the filename of the rendered video to stop it from overwriting your first attempt. To do this, change `animation.h264` to something else.

