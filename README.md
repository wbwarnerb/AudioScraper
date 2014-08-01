#Project Description
Making use of the PyShark Python library, I put together a simple script that performs some useful RTP stripping.
It takes the RTP layer out and turns it into a RAW audio file.  This can be turned into a wav using a sox command like:
sox -t raw -r 8000 -v 4 -c 1 -U my_audio.raw my_audio.wav

## Notes
I did have to modify PyShark.  In Python3, the comments in remote_capture.py file had to be updated. The \Device\NPF was being interpreted
by Python, even though it was commented out... so it would error on \N.  By removing the comment or adding \\Device\\NPF this was resolved.

##Future Improvements
- I would like to find a python library to do the audio conversion to remove the dependency on sox.
- Make this OO
- Other methds to pull out other parts of the pcap (user defined)
- UI/GUI