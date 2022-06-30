# docker-runelite

simple noVNC with runelite. Uses port 6080 for http.

deploy:
```
docker run --name="runelite" --restart="always" dylanve115/runelite
```
## Environment variables:
### Required:
PASSWORD = VNC Password

SCREENSIZE = (By default: 1280x800x24) Screen resolution of virtual screen.
Size of Runelite window cant be changed in runelite settings.

DISPLAY = (By default :20) Changes display number. No need to ever change this.

## Issues that I know:
### Sometimes doesnt boot:

Just start it again until it keeps running. not sure why it does this.

### The login link doesnt work when logging into runelite: 

Just open the docker console and install a web browser and run the web browser on display :20
```
apt-get update && apt-get install -y firefox-esr && firefox-esr
```
You can recreate the container after login and you will still be logged in.
