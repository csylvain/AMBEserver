##AMBEserver

This repository was created to make a tidy "just the server, testing tools, and AMBE transcoding tools" collection.

AMBEserver was not easy for me to find when I first heard of it. AMBEserver so useful, though, I think it should be easier to find using a search engine. With that done, it should be much easier to promote its wider use. I prompted the author of sdrangel to add support for AMBEserver, for instance.

I have contributed to the collection a utility to exercise a AMBE chip dongle or an AMBEserver. The work to port a prior AMBEtest script to python3 is my own. The ported, improved, and updated script supersedes those originally written by Hans DL5DI and those subsequent to them.

# Compiling

```
cd AMBEserver
./configure
make
make install
```

