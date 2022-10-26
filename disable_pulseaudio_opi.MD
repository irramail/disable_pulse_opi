# How to disable pulseaudio on OrangePI PC and change audio device for mplayer through the config

```sh
~/.xsessionrc
#Should to comment third line
pulseaudio --start => #pulseaudio --start
```

```sh
/etc/pulse/client.conf
#uncomment and change yes to no
;autospawn = yes => autospawn = no
```

```sh
cat .mplayer/config
#add thils line to mplayer config
ao=alsa:noblock:device=hw=0.0
```

