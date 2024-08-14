# *NOTE*
*This is a modified version based on [MSVPVF v1.3](https://github.com/mrpapersonic/msvpvf). I didn't make too many changes to the original code, but simply adapted it to my own preferences!*

*Here's the result of my compatibility test:*

Gen 1 | Gen 2 | Gen 3 | Gen 4 (?) | Gen 5 (?) | Gen 6 (?) | Gen 7 (?)
--- | --- | --- | --- | --- | --- | --- 
8.0 - 11.0 | 12.0 - 14.0 | 15.0 - 16.0 | 17.0 | 18.0 | 19.0 - 21.0 build 208 | 21.0 build 300 - Now

*__For the build numbers are more complicated, it does NOT mean that these versions are necessarily compatible.__ I only used the following build numbers for testing: ```15 build 416```, ```16 build 307```, ```17 build 387```, ```18 build 527```, ```19 build 651```, ```20 build 411```, ```21 build 208```, ```21 build 300```, ```22 build 93```. In particular, for 21 build 300+ projects, if they are audio-only projects, that is, their timelines do NOT contain any video events, they can be smoothly converted to 21 build 208- projects, otherwise not. Similar inconsistencies may occur with other build numbers, but I don't have the energy to test them one by one.*

*There are two versions of GUI in English and Chinese. To build an English one, use ```make gui```; To build a Chinese one, use ```make guicn```.*

<br>**This is the original README.md:**

# msvpvf
This repository has moved to [sourcehut](https://sr.ht/~mrpapersonic/msvpvf/). All future development will happen there.

C port of [msvpvf](https://archive.org/details/msvpvf-1.3-movie-studio-vegas-pro-version-faker-msvpvf-updated-to-1.31-focus-on-vegas)

![msvpvf CI](https://github.com/mrpapersonic/msvpvf/actions/workflows/build.yml/badge.svg)

## What is this??
msvpvf is a tool used to "downgrade" VEGAS Pro project files, written entirely in C. It has no runtime libraries, making it incredibly lightweight. Binaries for OS X and Windows are less than a megabyte in size.

Currently, the GUI doesn't look that great. Making pretty apps with `windows.h` is not the easiest job in the world; if someone is willing enough to make it look prettier, be my guest.

It is based on an old tool under the same name that was written in C#/.NET, but the original website is now down and it hasn't been maintained in over 2 years.

# Compatibility
There are 3 generations of modern Vegas project files:

Gen 1 | Gen 2 | Gen 3
--- | --- | ---
8.0 - 11.0 | 12.0 - 14.0 | 15.0 - Now

Any version in Gen 3 cannot be ported to Gen 2, and Gen 2 cannot be ported to Gen 1. That's just too complicated for a simple bit modifier. **However**, any file created in an older Vegas will work in a newer one.

## Compilation
```
git clone https://github.com/mrpapersonic/msvpvf
cd msvpvf
make
```

NOTE: if you are using Windows, there is a GUI available. To compile it, use `make gui`.
