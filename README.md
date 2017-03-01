# devastator

<<<<<<< HEAD
./devastator [optional flags] -d <device>
=======
./devastator <i>device node</i>
>>>>>>> a3b8151d348817e1a5709e53816ccfe77713da99

Flags:
-0 Perform an additional final zero pass
-c <count> Performing multiple passes 
-h Return something approximating help

A <i>quick</i> and <i>dirty secure</i> drive scrubber for FreeBSD but with 
minor tweaks should be usable anywhere sensible.

Quick, because it's faster than /dev/random
Secure, because it's less likely to be defeated than /dev/zero
Dirty, because it's a bit slapdash

It scrawls over your entire disk with a blowfish generated pile of 
pseudorandomness. A one time key is generated from urandom and a stream of
/dev/zero is encrypted over your beloved data.

One pass will render any information on the device unretrievable by any mortal 
methods, subsequent passes ensure the probability of useful recovery approach
zero.

<<<<<<< HEAD
It will be apparent to anyone inspecting the surface of the disk that it has 
been encrypted, possibly scrubbed although I think the final zero pass may 
mitigate this.
=======
Note: It will be apparent to anyone inspecting the surface of the disk that
it has been encrypted, possibly scrubbed. 

todo:	Optional multiple passes.<br>
todo:	Optional final zero pass.<br>
>>>>>>> a3b8151d348817e1a5709e53816ccfe77713da99
