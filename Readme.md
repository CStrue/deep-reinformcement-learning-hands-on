Execute container with tensorboard port exposed:

docker run --rm -it -v C:\Users\M0167078\Desktop\reinforcement-learning\own:/own -p 0.0.0.0:6006:6006 reinforcement-learning:latest /bin/bash

Xvfb :0 -screen 0 1024x768x24 -ac +extension GLX +render -noreset &> xvfb.log &
export DISPLAY=:0

Run xvfb: 
#this doesn't record mp4 files
xvfb-run "-screen 0 640x480x64" -a python3 04_frozenlake_nonslippery.py

#this does record mp4 files
Xvfb :0 -screen 0 1024x768x24 -ac +extension GLX +render -noreset &> xvfb.log &
export DISPLAY=:0
xvfb-run -a python3 04_frozenlake_nonslippery.py