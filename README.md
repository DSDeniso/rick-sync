# rick-sync
Syncs the music video of Never Gonna Give You Up across site visitors.

For Exile Jam 2019 i wanted to work on a light project. The act of syncronizing music or video across devices had long been on my mind due to the fact that I hadn't seen it done anywhere. Prior to this, I made an infoscreen demo using Raspberry Pi's utilizing the same technique. Therefore, I already had a good idea of what needed to be done, making the work mainly be about implementing it on a website, in Javascript -- and with Rick Astley this time. This would allow it to be easily accessed by anyone.

# The power of NTP
I think most people are unaware of the fact that NTP is crazy precise. For what I know it is black magic and I marvel at its capabilities. I embrace my mortality and accept that I might never get to know.

The script basically gets a Unix timestamp from the system and with the duration (in milliseconds) of Never Gonna Give You Up uses a modulo function to determine the location of the video if it has been looping since 0 Unix time.

# TODO
The video is currently not in sync across all devices. Apple devices seem to do well together, and I think the issue might be in different devices using different NTP server.

Next step would be determining whether it is possible for the script to retrieve the timestamp from a pre-specified server instead of the system. This will hopefully make all clients be in sync.
