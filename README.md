# Experiment: HapticBeats

Can we create a cool experience by combining haptic feedback with the beats of a song?

## Requirements

- Xcode 8.3
- iOS 10.1+
- Any iPhone with a vibration motor (although 7 is preferred, and 6s is better than older)

## How it works

Currently it's actually pretty terrible in how it works. It just checks the peak sound output for all the channels and compares it to the last check. If there was a huge spike, it plays a haptic feedback (which can be hard or soft, depending on intensity of spike). This would be fine for music that is just all beats, but music with other sounds (vocals, high-pitched instruments) tend to get in the way of this. It would probably be a good idea to switch to a better beat detection algorithm/library.

We currently only support songs that are not from Apple Music, have no DRM, and are downloaded on the device. An earlier version used the actual Music app's playback methods, but we had to switch. See if it's possible to maybe meter the output of the Music app.

Also, the code isn't the greatest. For reference, it was written from 1-3 AM as a fun experiment.

Enjoy :)
