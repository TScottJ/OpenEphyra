OpenEphyra
==========

**Update: August, 2019**

FYI, I've not been active in this repository since 2014 and understand it has fallen into disrepair, especially with respect to changes made to the Azure API. Apologies that I'm not able to respond to issues or other requests. I will, however, leave the repo here for the time being, in case someone finds it useful.

ScottJ

_____

This repository contains a resurrected and repaired version of OpenEphyra
<https://mu.lti.cs.cmu.edu/trac/Ephyra/wiki/OpenEphyra>. It was branched
from the latest version of OpenEphyra on SourceForge
<http://sourceforge.net/projects/openephyra/>, as of March, 2014, for use
in the OpenCog artificial intelligence system (Copyright (C) 2014
[OpenCog Foundation](http://www.opencog.org/)).

Changes made from the original:
- Removed obsolete KnowledgeMiner classes, which no longer function due to
changes in the various search engine APIs. Google, Bing, and Yahoo all have
since converted to subscription based services, as well as newer technology.
- Replaced the old Bing KnowledgeMiner with a new, functioning Bing Azure
KnowledgeMiner. This KM requires an Azure subscription key:
https://datamarket.azure.com/dataset/bing/searchweb. Currently, there is
a free key available that allows up to 5,000 queries per month.
- Miscelaneous minor fixes and clean-up.

The simplest way to open/build/run OpenEphyra is using Eclipse with the Ant build file feature. In Eclipse, select "File->New->Project->Java->Java project from existing ant buildfile" and choose the existing build.xml file that's in the project root. You can also use OpenEphyra in a sort of "API mode" if you want to call its functions from another app. The instructions for that are explained in the API_MODE.MD file (you still need to build the project first).

The original README file is included below:

==============================================================================
                      OpenEphyra Question Answering System

                        Nico Schlaefer (nico@cs.cmu.edu)
                           School of Computer Science
                           Carnegie Mellon University
==============================================================================
Copyright (C) 2007-2011 Carnegie Mellon University.

OpenEphyra is free software: you can redistribute it and/or modify it under the
terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

OpenEphyra is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
OpenEphyra. If not, see <http://www.gnu.org/licenses/>.

Acknowledgements:
-----------------

OpenEphyra was originally developed by Nico Schlaefer, but many others have made
valuable contributions. Special thanks go to:

- Guido Sautter, for his work on definitional QA and the NE recognizer.
- Justin Betteridge, who developed the answer type classifier.

Content of this Distribution:
-----------------------------

bin/           Java class files
cache/         Cache files
conf/          Configuration files
doc/           Javadoc documentation
lib/           Third party libraries
log/           Log files
res/           Resource files
scripts/       Command line scripts
src/           Java source files
build.xml      Ant build file for OpenEphyra
javadoc.xml    Ant build file for the Javadoc documentation
CHANGES        Changes made in new revisions
LICENSE        GNU General Public License
README         This file

Getting Started:
----------------

If you just like to run OpenEphyra in command line mode, try the following:

- Go to the folder 'scripts'.
- Execute OpenEphyra.sh (Unix, Linux, and Mac OS) or OpenEphyra.bat (Windows).
- Type in a factoid question, 'LIST:' followed by a list question, or 'exit'.

The only system requirements are a Java runtime environment (version 1.5 or
later) and about 1 GB of free RAM.

Documentation and Support:
--------------------------

The documentation and a collection of tutorials are hosted on the Ephyra site:
<http://www.ephyra.info/>.

Downloads of new releases and a discussion forum can be found at SourceForge:
<http://sourceforge.net/projects/openephyra/>.

If you would like to be notified of new releases and other important information
regarding OpenEphyra, you can subscribe to our mailing list:
<https://lists.sourceforge.net/lists/listinfo/openephyra-announce/>.

We highly appreciate any feedback, comments, and suggestions for improvements.
Please post to our forum or send an email to nico@cs.cmu.edu.

Sponsors:
---------

The OpenEphyra effort is supported in part by IBM Open Collaboration Agreement #W0652159.
