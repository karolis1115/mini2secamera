# mini2secamera 
A clone of [Android-FPVDemo](https://github.com/DJI-Mobile-SDK-Tutorials/Android-FPVDemo) with some modification to get the project up-to-date'ish
- Removed Some deprecated dependencies
- Fixed some warnings in code
- Updated out-of-date dependencies
- Updated to Gradle 8.2.1
- Updated DJI modules from 4.15 to 4.17
- removed Unused dependencies/ imports
- Removed android.tests and it's coresponding files & folders since it is deprecated and caused compile issues for newer dependencies or modules.
- Other minor code clean up
- Other minor code changes

# why the seperate repository?
And why name it **mini2se**camera? The "mini 2 se" is unsuported by the SDK dumdum...

Yes, DJI have not added SDK support for the mini 2 se as of 01/20/2024 and it is unclear if or when they will... -> [DJI SDK Forum](https://sdk-forum.dji.net/hc/en-us/articles/8818033368857-What-is-the-plan-for-the-consumer-level-aircraft) However, Considering that the "mini 2" and the "mini 2 se" do not differ by much at all, it might be possible to manually add support to the "mini 2 se", so ha, who's the dumdum now? (I am mentally insane)



## Why the optimism?
DJI mini 2 and mini 2 se use the same Remote Controller (DJI RC-N1) with their OcuSync 2.0 system.
Both drones have the same downward vision system and lack of obstacle avoidance system.
Both drones seem to have the same front facing image sensor, except that DJI purposley limited the max resolution and framerate to 2.7K @ 30fps for the mini 2 se
## Here are the potential issues.
- the mini 2 does have an additional front LED that the mini 2 se does not have.
- the mini 2's rear LED also doubles as a button that activates the "QuickTransfer" features which the mini 2 se does not support.
- As mentioned above the mini 2 se is limited to 2.7K @ 30 fps whereas the mini 2 can go upto 4K @ 30 fps, This limitation is most likely done on the firmware level, but who knows, maybe dji didn't bother and just removed the option in their "DJI Fly app"?
- the mini 2 se has a limited bitrate of 40 Mbps as opposed to the mini 2's 100 Mbps. (Could be the same situation as the resolution/framerate limit ?)
- Naturally the firmware is different between the mini 2 and mini 2 se. So it's possible (hopefully not) fimrware modification will be required.

# Here's what's interesting!
- Ignoring DJI's claim that the mini 2 se is unsuported and attempting to run it anyway reuslts in some interesting results that give hope to this goal!
  - The camera demo detects both that the controller is connected through USB and surprizingly it also detects that a drone is connected to the controller.
  - It's actually possible to get the demo app to stream video It's very unrealibale, only sucessfuly steaming video from the drone once in a blue moon after retrying multiple tries by relaunching and/or reconnecting controller to phone, restarting controller and/ or drone. So far I have not been able to get it to work consistently or narroe down the issue.
  - I have noticed that running DJI's [V4 sample SDK project](https://github.com/dji-sdk/Mobile-SDK-Android) the camera feed also ocasionally works.
  - in addition to that, warning messages can be seen when going to the coresponding demo menu. The messages I got were "bad compass cal" error (which was correct since I placed the drone near my laptop which has a metal body and contains magnets, same error was seen in the official app as well) and "Aircraft not connected" (even though it was).
  - The "Aircraft not connected" could possibly be due to the application receiving a model ID it does not recognise (shows "Unknown aircraft" in both the camera demo and SDK sample main menus)
 
  # Potentially usefull resources
- [DJI-Rev WiKi](https://wiki.dji-rev.com)
  - Comunity of people who are interested in hacking, reverse engineering, modifying, DJI products.
  - The wiki lists a lot of usefull infromation regarding that.
