# devastator

./devastator <device>

A quick and dirty "secure" drive scrubber for FreeBSD but with minor tweaks
should be usable anywhere sensible.

It scrawls over your entire disk with a blowfish generated pile of 
pseudorandomness. A one time key is generated from urandom and a stream of
/dev/zero is encrypted over your beloved data.

One pass will render any information on the device unretrievable by any mortal 
methods, subsequent passes ensure the probability of useful recovery approach
zero.

Note: It will be apparent to anyone inspecting the surface of the disk that
it has been encrypted, possibly scrubbed. 

todo:	Optional multiple passes 
	Optional final zero pass

