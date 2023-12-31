# Speech-Enabled Arithmetic Trainer: Leveraging Voice Recognition to Enhance Learning and Mental Acuity

This is a Python app using Tkinter and SpeechRecognition modules.

![](screenshot.png)

![image](https://github.com/Dhananjay-74x/Human-Computer-Interaction-HCI-Project/assets/86489966/a7a76fd4-5f40-4e0d-b38a-2b2e965e28ce)


The drill game shows a single digit multiplication and wait for uttered answer
(within 10 seconds).  Then the answer will be checked and the number of
correct/wrong answer will be tallied. The voice recognition is using the
`speech_recognition` module, which in turn, passed on to Google speech
recognition service.

## User experience

The performance is not as smooth as expected to be a "game". Two reasons for
that: It doesn't seem to be a way to capture audio and do recognition
simultaneously. Also, Google voice recognition is not instantaneous but with
some processing and network delay. These two added up, the user will see
noticible delay between calling out the answer and the answer being checked.

## Quality of voice recognition

The speech recognition module provides multiple ways to recognize. I tried out
the PocketSphinx and Google service. There are noticible difference between the
two: Firstly, PocketSphinx has way lower accuracy than Google's voice
recognition service, even after providing a dictionary with weight and so forth.
Secondly, the result from PocketSphinx is in spelled English words for numbers,
e.g., "forty two" while Google gives you numerials, "42". Even PocketSphinx is
offline, it doesn't seem to be any faster than Google.
