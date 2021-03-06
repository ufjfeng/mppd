# Introduction
A minimalistic python podcast downloader

Aimed to download old NPR Planet Money podcasts provided by [this repo](https://github.com/xjcl/planetmoney-rss),
will test on other feeds in the future

PodcastDownloader downloads podcasts from general RSS reeds, NPRPodcastDownloader downloads only NPR podcasts, 
also downloads transcript when available. 

Downloaded NPR contents are for 
[Personal Use Only](https://www.npr.org/about-npr/179881519/rights-and-permissions-information)

Requires feedparser

Audiobook build scripts requires [Audiobook Binder](http://bluezbox.com/audiobookbinder.html), make sure the `abbinder` is in your `$PATH`

# Example
```bash
$ python PodcastDownloader.py --year -r {podcast_feed}
```

# Known Issue

* `abbinder` may throw segfault at chapter building phase at the end of file conversion, especially when chapter list is long
* Life Kit feed won't be included in `npr_podcasts.json` automatically because it has a different url pattern. It can be manually added though.
