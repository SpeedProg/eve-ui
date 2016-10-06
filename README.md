# eve-ui
A nearly standalone (EVE Online) fit display script for inclusion in arbitrary websites.

https://quiescens.github.io/eve-ui/examples.html to see what it looks like by default, view source to see how it works.

With the impending removal of the in game browser, the old shortcut of using IGB links to display ship fittings will no longer be available. 
This script can be loaded in an arbitrary HTML document to automatically generate viewable, copy-pasteable fit windows for any element that it detects as a fit.

* Does not require any particular server side infrastructure on your part.
* Requires jQuery to be loaded before this script.
* Pulls item info from CCP's own CREST which should (theoretically) always be up to date.

At present, the script should work with almost any element that has a data-dna / data-itemid / data-charid attribute containing the appropriate values (dna string or itemid), or links with a href starting with "fitting:" / "item:" / "char:", such as:
* \<img src="blah" data-dna="fitting:670::" />
* \<div data-dna="fitting:670::">Pod\</div>
* \<a href="fitting:670::">Pod\</a>
* \<a href="item:27740">Vindicator\</a>
* \<a href="char:90788766">CCP Testguy1\</a>

The data- format is more flexible, but the href format can be useful for supporting forums or CMS's where users might only be allowed to post URLs, or where you already have links on a site and only need to change the href.

Getting the DNA string for a fit is left as an exercise for the reader, see:
* Pyfa
* https://o.smium.org/
* https://www.fuzzwork.co.uk/ships/dnagen.php
* Copying ingame text from a notepad or chat also works if you know how
