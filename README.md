# Girl Life (ЭТО) [English Community Version] - github edition

## Formatting comments when posting commits
Please use one of the following terms:
* fixed
* changed
* added
* removed
* text edit
Added and removed are for files being added or removed, fixed is for bug/code fixes, changed is for when events are changed and text edit is for changes to the text that'll appear on screen.
These are for searching to aid those working on the files.
Can you also include filenames (unless its a large number of files) and include any description you feel will help.
If adding content that is disabled (due to being WIP) can you comment in the file that its disabled and include your name so that it doesn't get activated in error.

## Quick start (for Unixy machines)
* clone/fork the repo
* make edits to the files in `locations`
* run `./txtmerge.py locations glife.txt`
* run `wine txt2gam.exe glife.txt glife.qsp`
* test that it works
* commit your changes
* push and/or send a pull request

## Quick start (for Windows machines)
* Double click the MakeQSP.bat
* Enjoy :)

## What exactly is all this?
In an effort to make editing the text of Girl Life easier, I set up this repo. This is based on the english community version. There are two branches: `master` and `releases`. On the `master` branch I will keep my version of the game as I make edits, merge pull requests, etc. while the `releases` is where you'd get things that you expect to actually work.

## Where are the images?
Not here. Shouldn't you know this already?

## What is `glife.txt`?
It turns out that `glife.qsp` is not the friendliest format for this game, but if you use `qgen` you can export the game in what they call `TXT2GAM` format. This is how `glife.txt` is obtained. Note that this is a large text file encoded in UTF-16, so git still has some trouble with it.

## What are the python scripts?
Since `glife.txt` is large and in UTF-16, I wrote two scripts, one that splits this file into one file per location, and puts them in `locations` after turning them to UTF-8, another that takes the UTF-8 files from `locations` and generates a UTF-16 file in `TXT2GAM` format.

## I modified something in `locations`, ran the `txtmerge.py` script, now what?
Assuming you ran something like
    ./txtmerge.py locations glife.txt
you now need to turn `glife.txt` into a `qsp` file. On my system, I use `wine` to run `txt2gam.exe`, works quite well:
    wine txt2gam.exe glife.txt glife.qsp

## Where do I get `qgen` and `txt2gam.exe`?
* [qgen](http://qsp.su/index.php?option=com_content&task=view&id=46&Itemid=56)
* [txt2gam](http://qsp.su/index.php?option=com_content&task=view&id=52&Itemid=56)
