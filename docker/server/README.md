Kiwix serve Docker image
========================

With local ZIM file(s)
----------------------

* Download a ZIM file from <https://wiki.kiwix.org/wiki/Content>

* Given `wikipedia.zim` and `wiktionary.zim` reside in `/tmp/zim/`, execute the following:

```bash
docker run -v /tmp/zim:/data -p 8080:80 kiwix/kiwix-serve wikipedia.zim wiktionary.zim
```

With remote ZIM file
--------------------

```bash
docker run -e "DOWNLOAD=https://download.kiwix.org/zim/wikipedia_bm_all.zim" -p 8080:80 kiwix/kiwix-serve
```

Screenshots
-----------

![screenshot_1.png](https://github.com/kiwix/kiwix-tools/raw/master/docker/server/pictures/screenshot_1.png)
![screenshot_2.png](https://github.com/kiwix/kiwix-tools/raw/master/docker/server/pictures/screenshot_2.png)
