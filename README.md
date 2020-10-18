# EC601_Project3
implementing jitsi

# Jitsi Meet
## docker jitsi
this version require docker

### Running the app
1. inside docker-jitsi-meet, run "docker-compose up -d"
2. go to https://localhost:8443/

## jitsi in ubuntu
another implementation/installation of jitsi is on a ubuntu server (using AWS' EC2 instance)
you can try accessing it via "testingmyrtc.cloudns.cl"

however, the server is not applied with SSL certificate and therefore is on http

note: if the camera is not working when in the room. try going back to main page, then click on the setting (the gear icon) to configure the camera + microphone


## jitsi (the main app)
jitsi has their own application running at "https://meet.jit.si/"

## analysis on jitsi
### the interface
#### main page
![Image of jitsi main page](https://github.com/ronnakornRat/EC601_Project3/blob/main/image/jitsi_main.JPG)

The main page of jitsi-meet provides the textbox for inputing room name, which will be used to refer to the room later when someone tried to join it

The textbox also provide randomly generated room name which is a string of "normal" words appended together
for example "NervousWeedsConfineIndeed"

the room will be launched when user click the "GO" button. The room itself is refered by the main url appended with the room name
for example,  https://meet.jit.si/NervousWeedsConfineIndeed

#### the room
jitsi-meet provides a clean interface as shown below

![Image of jitsi meeting room](https://github.com/ronnakornRat/EC601_Project3/blob/main/image/jitsi_room.JPG)

### the security
#### the room
According to Jitsi (https://jitsi.org/security/), the meeting room is only created when first participant join the room and is destroyed once the last participant leave the room. This method make it so that the "meeting room" is harder to be identitied, since it will only come into existence when someone actually joins the room.

Meeting room in the Jitsi-meet can be accessed/refered to ONLY by its name. This also means that, as long as the person know the name of the meeting room, anyone can join in the meeting. Thus, the security of the meeting room is tied to the room name. If the name is harder to be guessed, the less likely someone malicious would be able to access them.
for example, the https://meet.jit.si/NervousWeedsConfineIndeed would be less likely to be targeted than https://meet.jit.si/mymeeting

Jitsi has stressed this issue of having a secure name by placing the auto-generated name in the main page that people can use to "securely" pick a name. The auto-generated names, as mentioned above, are strings of "normal" words appended together. The idea is that, according to jitsi, it is "easy to remember and read out loud on a phone call."

### other interesting aspect
According to Jitsi, "Jitsi models its meetings after in-person gatherings." As the result, no one in the "meeting" will have the exclusive power (to mute,kick,etc.) over the others. Instead, from the jitsi's model, everyone is the moderator. Thus, anyone can mute/kick anybody else. This might sound inconvenient at first, however, according to Jitsi, this also allows anyone in the meeting to solve technical issues like, someone forgot to mute/unmute themselves, a microphone was having noises, people didn't leave the meeting, etc. 

On the other hand, Jitsi also provided an option for anyone to host their own Jitsi-meet instance and configure it to suit their needs.


