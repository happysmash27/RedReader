SaidIt RedReader (for Android)
=======================

A [SaidIt](https://saidit.net) fork of RedReader, an unofficial open source client for reddit.

![Build Status](https://travis-ci.org/QuantumBadger/RedReader.svg?branch=master)
[![Translation status](https://hosted.weblate.org/widgets/redreader/-/svg-badge.svg)](https://hosted.weblate.org/engage/redreader/?utm_source=widget)

Features
--------

* Free and Open Source Software - no ads/tracking.
* Lightweight and fast
* Downloads are compressed to save bandwidth.
* Support for multiple accounts.
* Several themes such as Night mode (i.e. dark theme) and Holo
* Swipe posts left and right to perform customisable actions, such as
  upvote/downvote, or save/hide.
* Advanced cache management - automatically stores past versions of
  posts and comments.
* Two-column tablet mode (can be used on your phone, if it's big enough)
* Image and comment precaching (optional: always, never, or Wi-Fi only).
* Built-in image viewer, imgur album viewer, GIF player, and
  webm/mp4/gifv player.


Downloading
-----------

SaidIt RedReader is available for free on the Google Play store:

https://play.google.com/store/apps/details?id=org.saiditnet.redreader

[<img src="https://play.google.com/intl/en_us/badges/images/generic/en_badge_web_generic.png"
      alt="Get it on Google Play"
      height="80">](https://play.google.com/store/apps/details?id=org.saiditnet.redreader)


Translating
-----------

Please help us translate RedReader into new languages, or improve the translations for existing languages!

https://hosted.weblate.org/projects/redreader/strings/

[![Translation status](https://hosted.weblate.org/widgets/redreader/-/svg-badge.svg)](https://hosted.weblate.org/engage/redreader/?utm_source=widget)


Building
--------

RedReader is built using Gradle. Several dependencies are required (and
listed in build.gradle), but these are handled automatically if you use
Gradle.

Detailed instructions on building RedReader using IntelliJ IDEA are in
[BUILD.md](BUILD.md).

SaidIt/reddit open source porting guide
----------------------

E.g. instead of org.quantumbadger.redreader use org.saiditnet.redreader:

    $ git clone https://github.com/QuantumBadger/RedReader.git
    $ cd RedReader
    $ mv src/main/java/org/quantumbadger src/main/java/org/saiditnet
    $ find ./src -type f -exec sed -i -e 's/org.quantumbadger./org.saiditnet./g' {} \;
    $ find ./build.gradle -type f -exec sed -i -e 's/org\/quantumbadger/org\/saiditnet/g' {} \;

Configuration:

* Create a saidit/reddit open source user account for the app, admin/employee accounts cannot own the app
* In preferences -> apps create an 'installed app' which is read only with no secret key for anonymous/guest app users
* Set the app's `redirect url` to `http://rr_oauth_redir`
* Set RedReader's `CLIENT_ID` to the saidit/reddit app id

License
-------

RedReader is licensed under the GPL, version 3. A copy of the license is
included in [LICENSE.txt](LICENSE.txt).

Bitcoin donations are welcome and accepted at the following address:
`1874wapGxDo2vEp4avisda4gx3SCjsHCQJ`


Thanks
------

Thanks to:

* QuantumBadger and RedReader contributors
* tomorrowkey.jp, for the [GIF decoder](https://code.google.com/p/android-gifview/) (Apache License 2.0)
* Apache, for various libraries
* The [Jackson JSON processor](http://jackson.codehaus.org/)
* [Joda](http://joda-time.sourceforge.net/)
* [/u/fosterbuster](http://www.reddit.com/user/fosterbuster) for the Danish translation
* [/u/balducien](http://www.reddit.com/user/balducien) and [/u/andiho](http://www.reddit.com/user/andiho) for the German translation
* [remil19](https://github.com/remil19) for the French translation
* [Husam Bilal](https://github.com/husam212) for the Arabic translation
* [Juanma Reyes](https://github.com/jmreyes), [moshpirit](https://github.com/moshpirit), and Andrés Hernández for the Spanish translation
* [Martin Macko](https://github.com/LinkedList) for the Czech translation
* [klenje](https://github.com/klenje) for the Italian translation
* [Beleg-Cuthalion](https://github.com/Beleg-Cuthalion) for the Dutch translation
* [tjernquist](https://github.com/tjernquist) for the Swedish translation
* [Badita Viorel-Octavian](https://github.com/vooctavian) for the Romanian translation
* [András Lengyel-Nagy](https://github.com/lna91) for the Hungarian translation
