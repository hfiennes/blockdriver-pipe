# ARCbbs pipe module

ARCbbs supported "loopback" connections via a virtual pipe which was implemented as a module (for the buffering) and two block driver "ends" - PipeA and PipeB.

Anything sent on PipeA would arrive in the rx buffer of PipeB and vice-versa. Backpressure was provided by the buffer in the module filling, so it worked mostly seamlessly as I remember.

I believe this is the source to all 3 parts, dug out of an old hard disk image that I managed to get to mount in Linux. I used https://github.com/ksherlock/bbc-list/ to convert the basic files to text so they're more readable in the github context.
