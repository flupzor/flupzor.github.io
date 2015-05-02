---
layout: post
title:  "Abbott stuff"
date:   2010-12-19 16:00:00
tags: [diabetes, reverse engineering]
---

I've been trying to figure out the protocol for the Abbott Freestyle product
line. I made a protocol description which can be found [here][abbott-protocol].

If you're looking for the description for the Abbott Xceed product line, Chris
Ridd made an awesome description which can be found [here][xceed-protocol]. He
also made an implementation in Objective C, but I haven't found time to test
that.

Abbott sells an adapter cable which uses the TI 3410 chipset. This chipset is
supported by most modern operating systems, however not all include the Abbott
vendor id/product id (0x1a61, 0x3410 respectively). Currently it should work by
default in Windows XP using the driver Abbott supplied, and in OpenBSD since
[this][openbsd-abbott] commit. Getting it working with other operating systems
should be trivial.

[abbott-protocol]: protocol.html
[xceed-protocol]: http://www.lnv.pwp.blueyonder.co.uk/xceed/
[openbsd-abbott]: http://marc.info/?l=openbsd-cvs&m=129261992926939&w=2
