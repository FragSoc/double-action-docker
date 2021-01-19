A docker image for running a dedicated server for the game [Double Action: Boogaloo](https://store.steampowered.com/app/317360/Double_Action_Boogaloo/). This Dockerfile uses [CM2Walki's](https://github.com/CM2Walki/) SteamCMD base image.

# How to use this image
## Simple usage (recommended)

Clone this repository locally:<br/>
```console
$ git clone https://github.com/FragSoc/double-action-docker.git
```

Create a new directory for the game installation:
```console
$ mkdir -p $(pwd)/dab-data
$ chmod 777 $(pwd)/dab-data # Makes sure the directory is writeable by the unprivileged container user
```

**Make necessary edits to the docker-compose.yml**
**Look at environment variable section below for guidance.**

Run docker-compose up:<br/>
```console
$ docker-compose up
```


**The container will automatically update the game on startup, so if there is a game update just restart the container.**


## Environment Variables
You can overwrite these values within the docker-compose file, below are the defaults: 
```dockerfile
SRCDS_PORT=27015 # The port on which the server communicates on
SRCDS_TOKEN=0 # You will need this to be public
```
