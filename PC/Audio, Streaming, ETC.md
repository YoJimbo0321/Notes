# PC - Audio, Streaming, ETC

# Links

- [VB-Audio VoiceMeeter Banana](https://vb-audio.com/Voicemeeter/banana.htm)
- [VB-Audio VB-Cable](https://vb-audio.com/Cable/index.htm)
- [VoiceMeeter Virtual Inputs/Outputs (VAIO)](https://voicemeeter.com/quick-tips-voicemeeter-virtual-i-os/)
- [Advanced Audio Streaming Elite Dangerous and ALL Games with Voice Meeter, OBS and Discord (Guide)](https://youtu.be/b5TpjNmkRYY)
- [Separate Game Audio, Discord, Music in OBS! (A Voicemeeter Tutorial For Beginners)](https://youtu.be/XD9sWOjITYU)
- [How to Remove Discord Voice Chat from Your OBS Stream (JP)](https://arutora.com/15444)
- [Use VoiceMeeter with VB Audio Cable for Skype, Zoom or Discord](https://voicemeeter.com/use-voicemeeter-with-vb-audio-cable-for-skype-zoom-or-discord/)
- [Mute Discord notification sounds while streaming using Voicemeeter Banana + Voice Audio Cables (VAC)](https://youtu.be/SSNtcn6urWc)
- [Reducing Audio Latency in VoiceMeeter](https://www.youtube.com/watch?v=LAYKcIC5iFY&feature=youtu.be)
- [OBS Studio - Wiki](https://obsproject.com/wiki/)
- [OBS Studio - Basic Setup Guide](https://youtu.be/tl4J4GGpflA)
- [OBS Studio - NVENC Output Setup](https://youtu.be/JmGQ6X8d0Y8)
- [OBS Studio - Replay Buffer (Shadowplay) Setup Guide](https://youtu.be/oSI_KA4Q8gA)
- [OBS Studio - Advanced Recording Guide With Multi Track Audio](https://obsproject.com/wiki/Advanced-Recording-Guide-With-Multi-Track-Audio)
- [OBS Studio - Filters Guide](https://obsproject.com/wiki/Filters-Guide)
- [OBS Studio - Plugins](https://obsproject.com/forum/resources/categories/obs-studio-plugins.6/)
- [Streamlabs Stream Widgets](https://streamlabs.com/widgets)
- [Streamer's Haven - Why the OBS Noise Gate is an undesirable filter](https://streamershaven.blog/software/obs-tutorials/obs-noise-gate/)
- [Twitch Suggested OBS Encoding Settings](https://stream.twitch.tv/encoding/)
- [NVIDIA NVENC OBS Guide](https://www.nvidia.com/en-us/geforce/guides/broadcasting-guide/)
- [NVIDIA Broadcast Setup](https://www.nvidia.com/en-us/geforce/guides/broadcast-app-setup-guide/)
- [What Can I Do With Elgato Stream Deck](https://www.youtube.com/watch?v=POt4-8b0iPE)
- [iZOTOPE - Gain Staging: What It Is and How to Do It](https://www.izotope.com/en/learn/gain-staging-what-it-is-and-how-to-do-it.html)

# Adjusting Microphone Gain

- Control Panel > Sound > Recording > Microphone > Properties > Levels > Increase microphone gain
- Increasing your gain at the source is the best way to boost your mic volume, but you should only boost the gain up to a point before it begins to significantly amplify background noise.
- After setting this baseline gain level, you can further boost it in software (ex. applying Gain in OBS)

# VoiceMeeter

## Windows Sound Setup

- Control Panel > Sound > Playback > Set VoiceMeeter Input as Default Device
- Control Panel > Sound > Playback > Set VoiceMeeter Aux Input as Default Communications Device
- Control Panel > Sound > Recording > Set VoiceMeeter Output as Default Device
- Control Panel > Sound > Recording > Set VoiceMeeter Aux Output as Default Communications Device
- *Settings > System > Sound > App volume and device preferences (Can separately set audio input/output to something other than the default for applications that don't let you change them within their own settings (ex. routing internet browser audio to a Virtual Cable))* (Optional)

## Basic VoiceMeeter Settings

- Menu > Check "Auto Restart Audio Engine"
- Menu > Check "System Tray (Run at Startup)"

## Audio Input/Output Setup

- Begin with A1 through B2 unchecked for all Hardware Inputs and Virtual Inputs.
- Hardware Out A1 > Select primary headphones/speakers (Choose the WDM version if available for best performance and lowest latency)
- Hardware Input 1 > Change name to "Mic"
- Hardware Input 3 > Change name to "Discord"
- VoiceMeeter VAIO > Change name to "Desktop"
- VoiceMeeter AUX > Change name to "Voice"
- Mic > Select microphone input (Choose the WDM version if available for best performance and lowest latency)
- Discord > Select CABLE Output (VB-Audio Virtual Cable) (effectively creates another Virtual Input to use for selectively routing audio in OBS or other applications)
- Discord, Desktop, and Voice > Check: A1 (Sends incoming audio to Hardware Out A1)
- Mic > Check: B2 (Sends incoming audio to VoiceMeeter Aux Output)

### Source Aliases

- Mic = VoiceMeeter Aux Output
- Discord = CABLE Output
- Desktop = VoiceMeeter Input
- Voice Chat = VoiceMeeter Aux Input
- *Browser/ETC = VoiceMeeter VAIO3 Input* (Optional, if using VoiceMeeter Potato)

## In Discord

- Settings > App Settings > Voice & Video > Input Device: VoiceMeeter Aux Output
- Settings > App Settings > Voice & Video > Output Device: CABLE Input
- Settings > App Settings > Streamer Mode > Check "Automatically Enable/Disable"
- Settings > App Settings > Streamer Mode > Options > "Hide Personal information" ON
- Settings > App Settings > Streamer Mode > Options > "Hide Invite Links" ON
- Settings > App Settings > Streamer Mode > Options > "Disable Sounds" OFF
- Settings > App Settings > Streamer Mode > Options > "Disable Notifications" ON
- (In Windows) Settings > System > Sound > App volume and device preferences > (Find the volume slider for Discord notification sounds) > CABLE Input

## In Games And Other Voice Applications

- (Voice Chat) Input Device: VoiceMeeter Aux Output
- (Voice Chat) Output Device: VoiceMeeter Aux Input

## Reducing Audio Latency

- (In Sound Control Panel, for each device) Properties > Advanced > Default Format > Match the sample rate of all input and output devices (ex. if mic goes up to 48 kHz, match other devices at 48 kHz)
- VoiceMeeter Banana > Menu > System Settings/Options > Make sure that the sample rate of all input and output devices match.
- VoiceMeeter Banana > Menu > System Settings/Options > Try lowering buffer size (256 is probably safe)

## Troubleshooting

- If having issues with audio, try Menu > "Restart Audio Engine"

# OBS

## Settings

### General

- Output > Check: "Show confirmation dialog when starting streams"
- Output > Check: "Show confirmation dialog when stopping streams"
- Output > Check: "Show confirmation dialog when stopping recording"
- Output > Check: "Automatically record when streaming"
- Output > Check: "Keep recording when stream stops" (useful for if/when your stream gets disconnected)
- Output > Check: "Automatically start replay buffer when streaming" (needs replay buffer enabled to toggle, see Output)
- Output > Check: "Keep replay buffer active when stream stops"
- System Tray > Check: "Enable"
- Studio Mode > Check: "Transition to scene when double clicked"

### Stream

- Setup as necessary with preferred service(s)

### Output

- Output Mode: Advanced
- Streaming > Audio Track: 1 (the default audio track for the stream that all audio sources should output to)
- Streaming > Encoder: NVIDIA NVENC H.264 (if available)
- Streaming > Uncheck: "Rescale Output"
- Streaming > Rate Control: CBR
- Streaming > Birate: 6000 Kbps (for 1080p 60fps with an 8+ Mbps upload speed)
- Streaming > Keyframe Interval: 2
- Streaming > Preset: Quality
- Streaming > Profile: high
- Streaming > Uncheck: "Look-ahead" (exceptions exist but typically leave it off)
- Streaming > Check: "Psycho Visual Tuning" (exceptions exist but typically leave it on)
- Streaming > GPU: 0 (always set to 0 on single GPU systems)
- Streaming > Max B-frames: 2
- Recording > Recording Path: Set to desired location
- Recording > Recording Path > Check: "Generate File Name without Space"
- Recording > Recording Format: mkv
- Recording > Audio Track: Check all audio tracks being used
- Recording > Encoder: NVIDIA NVENC H.264 (if available)
- Recording > Rate Control: CQP
- Recording > CQ Level: Between ~16-22 (LOWER is higher quality; default is 20)
- Recording > Keyframe Interval: 0
- Recording > Preset: Quality
- Recording > Profile: high
- Recording > Uncheck: "Look-ahead"
- Recording > Uncheck: "Psycho Visual Tuning"
- Recording > Max B-frames: 2
- Audio > Track X > Audio Bitrate: 160 (default; may want to adjust based on upload speed, file size requirements, streaming service requirements, etc.)
- Replay Buffer > Check: "Enable Replay Buffer"
- Replay Buffer > Maximum Replay Time: 300s (or desired length) (IMPORTANT: also need to set a hotkey to Save Replay)
- Replay Buffer > Maximum Memory > 512 MB (default)

### Audio

- General > Sample Rate > Match the sample rate of all input and output devices (typically 48 kHz)
- Global Audio Devices > Set all to "Disabled" (use Audio Input/Output Capture Sources instead)
- *Advanced > Monitoring Device > Whatever output you want to use for monitoring* (Optional)

### Video 

- Base (Canvas) Resolution > Match to the resolution of the content (ex. resolution of the monitor, resolution of the game window)
- Output (Scaled) Resolution: 1920x1080
- Downscale Filter: Lanczos or Bicubic
- Common FPS Values: 60

### Advanced

- Process Priority: Normal

## Studio Mode

- Transition > Uncheck: "Swap Previous/Output Scenes After Transitioning"

## Audio Mixer

- Advanced Audio Properties > Audio Monitoring > Turn on when needed
- Advanced Audio Properties > Tracks > Assign as necessary (all relevant audio sources should at least go to the Track used by the stream)

## Sources

- Game Capture > Properties > Mode: Capture any fullscreen application > Check "Use anti-cheat compatibility hook" when needed
- Window Capture > Properties > Capture Method > Select "Windows 10" if having issues capturing a window

## Other Shortcuts/Tips

- Alt+click and drag to resize the bounding box.
- Ctrl+E to more granularly adjust the transform.

## Streaming to Discord

- Right click the preview > Windowed Projector (Preview) > Stream the window on Discord

# NVidia Broadcast (Optional)

- (Note, may introduce noticeable delay to microphone audio)
- Microphone > Microphone Source: Select microphone input
- Microphone > Effects > Noise removal: On
- (In VoiceMeeter) Swap Mic input to "Microphone (NVidia Broadcast)"

#pc
#settings
