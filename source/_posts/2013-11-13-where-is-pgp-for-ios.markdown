---
layout: post
title: "Where are PGP tools for iOS?"
date: 2013-11-13 09:03
comments: true
categories: 
---
Is any one using PGP on iOS? The options seem extremely limited. 

Despite the fact that PGP has been around for decades, PGP support on iOS is quite limited. It is readily available on traditional computers (see [Prism Break](http://prism-break.org/) for an exhaustive list), but what about iOS?

Most PC applications seem to simply provide a frontend for [GPG](http://www.gnupg.org) via a mechanism like [GPGME](http://www.gnupg.org/related_software/gpgme/index.en.html). This approach avoids the pitfalls of rolling your own crypto, but it means that GPG must be available. However, the design of iOS precludes launching another user process from within an app. And, since GPG is licensed under the GPL, which [may conflict with Apple's terms of service](http://www.fsf.org/blogs/licensing/more-about-the-app-store-gpl-enforcement), there is little incentive to put a lot of effort into this 

The result of these two problems means that there is not yet a good option for developers who want to support secure email.

Even with these problems there are a couple apps available, though it isn't apparent what crypto libraries they are using.

## iOS Apps:

- **[iPGMail](http://ipgmail.com/)** might be a good option. The app store screen shots only show the key management features, but reviews are good. 
- **[oPenGP](https://itunes.apple.com/us/app/opengp/id414003727)** seems to be based on copying/pasting for encryption/decryption. Single review mentions crashing.


## Related libraries:

- **[GPGME](http://www.gnupg.org/related_software/gpgme/index.en.html)** is an interface to the GPG binary. It might be possible to port GPG/GPGME to the iPhone, but the design of this library is based upon starting GPG as it's own process, which is forbidden by iOS. GPGME is licensed under the LGPL, but GPG is GPL'd, possibly making it unsuitable for App Store distribution. 
- **[UNNetPGP](https://github.com/upnext/unnetpgp)** is based on NetPGP, the NetBSD PGP library. The BSD license is a better option for many apps, but NetPGP has not seen any active development since 2010. UUNetPGP still has some rough edges to be flushed out, but looks very promising if the underlying library is maintained.
- **[libgcrypt](http://www.gnu.org/software/libgcrypt/)** is an actively maintained, LGPL, general purpose crypto library. However, it is *only* a crypto library. It doesn't handle keyring management and requires *much* more knowledge of crytpo on the part of the developer.
