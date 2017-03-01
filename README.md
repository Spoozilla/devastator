# devastator

./devastator [optional flags] -d &lt;device&gt;

Flags:<br>
-0 Perform an additional final zero pass<br>
-c &lt;count&gt; Performing multiple passes<br>
-h Return something approximating help<br>

A <i>quick</i> and <i>dirty secure</i> drive scrubber for FreeBSD but with 
minor tweaks should be usable anywhere sensible.

Quick, because it's faster than /dev/random<br>
Secure, because it's less likely to be defeated than /dev/zero<br>
Dirty, because it's a bit slapdash<br>

It scrawls over your entire disk with a blowfish generated pile of 
pseudorandomness. A one time key is generated from urandom and a stream of
/dev/zero is encrypted over your beloved data.

One pass will render any information on the device unretrievable by any mortal 
methods, subsequent passes ensure the probability of useful recovery approach
zero.

It will be apparent to anyone inspecting the surface of the disk that it has 
been encrypted, possibly scrubbed although I think the final zero pass may 
mitigate this.

