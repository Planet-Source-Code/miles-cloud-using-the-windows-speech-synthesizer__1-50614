<div align="center">

## Using the Windows Speech Synthesizer


</div>

### Description

This article explains how to use the windows speech synthesizer, which can be useful sometimes, such as in programs that have an Impaired person help option. Note: to use this, you have to have a speech synthesizer installed, but usually XP has one automatically.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Miles Cloud](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/miles-cloud.md)
**Level**          |Beginner
**User Rating**    |4.8 (19 globes from 4 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Sound/MP3](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/sound-mp3__1-45.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/miles-cloud-using-the-windows-speech-synthesizer__1-50614/archive/master.zip)





### Source Code

```
This is only the basics, because I figured out how to use it today, but it still does what it is supposed to.
First of all, open a new project, Doesn't matter what kind, and click Project|Referances, and look for "Microsoft Speech Object Library". Check the box by it, and click OK. This is to basically connect the DLL to you're project. Once you did, Open the code window, and go to the Declarations section. In it, type:
Public Voice As New SpVoice
Public VoiceStatus As New ISpeechVoiceStatus
Now, whenever you want Windows voice synthesizer to say something, use a line of code like this:
Voice.Speak "This is an example of how to use Microsofts Voice Synthesizer"
You can replace the text in the parenthesis with ANYTHING, including variables and other various information. Only one problem: It freezes the program until it's done speaking. This can be a major problem. How is it fixed? By adding a flag, called SVSFlagsAsync. This will allow the program to operate while it's speaking. So now, it's like this:
Voice.Speak "This is an example of how to use Microsofts Voice Synthesizer", SVSFlagsAsync
To Make it state the contents of a variable, you'd say something like this:
Voice.Speak LabelDescription.Caption, SVSFlagsAsync
-or-
Voice.Speak MyVariable, SVSFlagsAsync
Pretty simple eh?
That's all I could figure out so far, but I'll keep experimenting, and see what I can do. This might also work on older versions of VB, but I'm not sure, so even if you don't have Visual Basic 5 or 6, try it and tell us if it works. ^_^
```

