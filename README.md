Making use of the PyShark Python library, I put together a simple script that performs some useful RTP stripping.
It takes the RTP layer out and turns it into a RAW audio file.  This can be turned into a wav using a sox command like:
sox -t raw -r 8000 -v 4 -c 1 -U my_audio.raw my_audio.wav

##Improvements
- I would like to find a python library to do the audio conversion to remove the dependency on sox.
- Make this OO
- Other methds to pull out other parts of the pcap (user defined)
- UI/GUI