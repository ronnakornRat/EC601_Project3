# EC601_Project3
implementing jitsi

### Jitsi Meet
## docker jitsi
this version require docker

# Running the app
1. inside docker-jitsi-meet, run "docker-compose up -d"
2. go to https://localhost:8443/

## jitsi in ubuntu
another implementation/installation of jitsi is on a ubuntu server (using AWS' EC2 instance)
you can try accessing it via "testingmyrtc.cloudns.cl"

however, the server is not applied with SSL certificate and therefore is on http

note: if the camera is not working when in the room. try going back to main page, then click on the setting (the gear icon) to configure the camera + microphone


## jitsi (the main app)
jitsi has their own application running at "https://meet.jit.si/"

### analysis on jitsi
## the interface
# main page
The main page of jitsi-meet provides the textbox for inputing room name, which will be used to refer to the room later when someone tried to join it

The textbox also provide randomly generated room name which is a string of "normal" words appended together
for example "NervousWeedsConfineIndeed"

the room will be launched when user click the "GO" button. The room itself is refered by the main url appended with the room name
for example,  https://meet.jit.si/NervousWeedsConfineIndeed

# the room
jitsi-meet provides a clean interface as shown below

![Image of Yaktocat](https://github.com/ronnakornRat/EC601_Project3/blob/main/image/jitsi_room.JPG)

# the security