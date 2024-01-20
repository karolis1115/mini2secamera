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

# why the seperate repo?
- : -> The mini2se is unsuported by the SDK, why did you name it **mini2se**camera dumdum ?
 - Yes, DJI have not added SDK support for the mini 2 se as of 01/20/2024 and it is unclear if or when they will... [DJI SDK Forum](https://sdk-forum.dji.net/hc/en-us/articles/8818033368857-What-is-the-plan-for-the-consumer-level-aircraft)
   However, Considering that the "mini 2" and the "mini 2 se" do not differ by much at all, it might be possible to manually add support to the "mini 2 se" drone.
- **Considering that**
 - DJI mini 2 and mini 2 se Use the same Remote controller (DJI RC-N1) with their OcuSync 2.0 system
 - Both drones have the same  downward vision system and lack of obstacle avoidance system.
 - Both drones both appear to have the same front facing image sensor, except that DJI purposley limited the max resolution and framerate to 2.7K @ 30fps for the mini 2 se
- **Here's what is different**
 - the mini 2 does have an additional front LED that the mini 2 se does not have.
 - the mini 2's read LED also doubled as a button that activates the "QuickTransfer" features which the mini 2 se does not seem to support.
 - As mentioned above the mini 2 se is limited to 2.7K @ 30 fps whereas the mini 2 can go upto 4K @ 30 fps, This limitation is most likely done on the firmware level, but who knows, maybe dji didn't bother and just removed the option in their "DJI Fly app"?
 - the mini 2 se has a limited bitrate of 40 Mbps as opposed to the mini 2's 100 Mbps. (Could be the same situation as the resolution, framerate limit ?) 
