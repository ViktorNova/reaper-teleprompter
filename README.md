# Reaper Teleprompter

## Installation
Navigate to your REAPER resource folder in a terminal  
_you can find this by clicking Options > "Show REAPER resource path in explorer/finder"_  

Clone this repo into a new folder called "reaper_www_root":  
`git clone git@github.com:ViktorNova/reaper-teleprompter.git reaper_www_root`

_Note: if you already have a folder called reaper_www_root, just clone this repo somewhere else and copy the files into there_

Set up 2 new Web browser control interfaces from Reaper under Control/OSC/Web:
 - Choose "teleprompter.html" for the first, give it port 8100
 - Choose "lyrics-dark.html" for the second, give it port 8101

After that, just visit http://localhost:8100 in a browser. The lyrics-only page is available at http://localhost:8101

For remote access to the web interface from another device (phone/tablet/etc), you will need to edit like 950 in teleprompter.html, and change the URL of the lyrics iframe to be the IP or DNS name of the computer Reaper is running on, ideally static (or the rc.reaper.fm domain if you are using that. I haven't tested it that way). You'll also need to make sure that this isn't being blocked by a firewall on your system.  
Then visit on your remote device at: http://your.reaper.ip.address:8100



Follow these instructions to add lyrics/cues/etc using the lyrics editor:
https://youtu.be/TMZZvk4x93o?t=456

## Credits
This is a hacked up version of the "Fancier" and "Lyrics" web interfaces that are included with Reaper, I didn't write it. It's kind of messy, but works. The messiest part is that "lyrics" is embedded inside of "teleprompter" as an iframe (yuk), and the "fancier" interface that teleprompter was adapted from has a ton of events that have been stripped out of the UI, but are still processing track/etc data in the background, and some elemets are only being hidden with CSS. Ideally this extra stuff should be removed. This was a means to an end and works fine, but any help is welcome!

The included VT323 font is Copyrighted 2011, The VT323 Project Authors (peter.hull@oikoi.com)
