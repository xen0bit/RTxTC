# RTxTC

base_videos contains 30s videos color coded and labelled for easy testing.

Included in directory is PNG files and an OpenShot video project that can easily be used to create shorter/different clips.

root directory contains playlists in various different formats with relative paths.

VLC-Scheduler contains a modified version of https://github.com/EugeneDae/VLC-Scheduler
`pip3 install -r VLC-Scheduler/requirements.pip`

Main config in vlcscheduler.yaml

Project is in python and should integrate easily with our existing tools. Primary use is injecting advertisement videos at certain intervals and it watches a "special" directory for any new files which are injected into the stream.
I'm working to see if the directory watcher can be hooked to react to websocket input and connect to an external source (one that we control)

VLC-SCheduler can be bundled to a binary for all platforms usin pyinstaller. This would allow us to distribute the binary to RT, they provide us the vlcscheduler.yaml, and we can handle running our own infrastructure over websockets or w/e.

If our server were to go down, or any other interruptions, RT stream would just play as normal (safe failure).