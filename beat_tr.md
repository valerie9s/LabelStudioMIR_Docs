---
title: Beat Tracking
layout: home
---
## Beat Tracking
DISCLAIMER: The workflow for this project is currently much more awkward than necessary. The ideal workflow would allow the user to tap along to the beat, effectively annotating the audio live. Unfortunately, LabelStudio has disabled many features that would make this possible... so for now this is what we have. 

**Automatic Beat Tracking** is a [traditional MIR task] which marks the temporal location of [beats], often also including downbeats (the first beat of a measure). This is equivalent to when you would tap your finger or your foot to a piece of music.

![](BeatMarkers.drawio.png)

Please use wired headphones or speakers for this task, since Bluetooth headphones can have a problematic amount of latency. We'd like for these annotations to be as accurate as possible, but we understand that sometimes there can be some uncertainty.  

<br>

**Instructions:**
 - Play audio clip
 - Follow the beat until you reach a beat that hasn't been marked yet (if just starting, mark the first occurance of a downbeat)
 - Pause at the next beat
 - Use hotkeys (1 for downbeat, 2 for beat) to select a label
 - Double click to place an annotation (Explanation of downbeat vs beat further down)
 - Start audio clip again a few beats back and repeat

<br>
  

**Issues:**

This is a list of known issues at the moment. Feel free to let me know if there's anything I've left out.

 - Playhead freezes or doesn't move 
    - This is an issue with our workaround for having instantaneous time markers. The display you interact with isn't actually a WaveSurfer element, but a time series plot aligned with the audio, making it a little buggy. If LabelStudio allows us to make live annotations, we can go back to using the WaveSurfer element, since they could just be submitted as time segments of very small length.
 - Beat doesn't play back, can't check annotation
    - This is the same issue as before, with the major roadblock being LabelStudio's disabled features for interaction with the audio element. 
 - Visual and sound out of sync
    - Same issue as playhead freezing.


----



[beats]: https://en.wikipedia.org/wiki/Beat_(music)
[traditional MIR task]: https://www.music-ir.org/mirex/wiki/2025:Audio_Beat_Tracking
