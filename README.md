# FIG - Feature Inspector Gadget

## What is it?

FIG is a [Google Gadget][0] used to inspect what gadget features are supported by a gadget container 
in which this gadget is run. This gadget also provides links to pages with additional
info (documentation and tutorials) about respective gadgets.

Knowing about what gadget features are available is useful for finding out what
a particular gadget container can support, which can be useful for:

- either finding new sites and social networks where your existing gadget may run
- discovering what features are available in a gadget container, some of which you might 
  (want to) use and make your gadget more compelling
- learning more about gadgets (using direct links to relevant documentation)

### Background

Originally, `gadgets.util.hasFeature` method from [OpenSocial API][1] was intended to be used
for checking what features are supported by the container. Unfortunately, this method is useless
in [Apache Shindig][3] since it **always returns true** for features that are declared by 
gadget itself and not whether gadget container actually supports the particular feature.
Such behavior is totally against the [gadget specification][2] which states:

"*The server **MUST** support the following core JavaScript API, which applies to <Optional> 
features:
`gadgets.util.hasFeature(featureName)`<br/>
As indicated in the JsDoc, this method returns true if the server is able to satisfy
**featureName**, false otherwise. Gadget developers can use this functionality to enhance their
gadgets if features are available without disabling their gadget if the features are missing.*"

This problem was worth the attention since [Shindig][3]
is the *reference implementation* of OpenSocial API specifications and **the most widely used
OpenSocial container implementation** on actual social networking sites.
The problem with `hasFeature` function has been observed in Shindig implementations
of the OpenSocial spec [until][4] and including [version 0.9][5].

Using FIG, gadget developers can learn which gadget features are actually supported by
a gadget container.

[0]: http://www.google.com/webmasters/gadgets/
[1]: http://code.google.com/apis/opensocial/
[2]: http://code.google.com/apis/gadgets/docs/spec.html
[3]: http://incubator.apache.org/shindig/
[4]: http://wiki.opensocial.org/index.php?title=Gadgets.util_%28v0.8%29#gadgets.util.hasFeature
[5]: http://wiki.opensocial.org/index.php?title=Gadgets.util_%28v0.9%29#gadgets.util.hasFeature

## More info

### Gadgets

More information about gadgets in general you can find here:
http://code.google.com/apis/gadgets/docs/spec.html

### Containers

OpenSocial containers are also gadget containers so any social networking site
supporting OpenSocial can also run this gadget.

Some of gadget containers in which you can run this gadget are: 

- social networking sites: MySpace, Orkut, LinkedIn, Ning, XING, etc.
- personalized home page: iGoogle
- web mail: Google Mail
- collaboration tool: Google Wave

Additional OpenSocial containers can be found at: [Container Information](http://wiki.opensocial.org/index.php?title=Main_Page#Container_Information)


## Authors
- Nenad V. Nikolic <nenad.nikolic@xing.com>
- Christopher Blum <christopher.blum@xing.com>


## Release notes

### Version 0.48
December 31, 2009

- Added StudiVZ features "cache", "vzflash", "invite", "tracking"
- Added "opensocial-payment" feature 
- Added a smaller screenshot
- Fixed "atlassian.util" feature detection

### Version 0.47
December 22, 2009

- Added license
- Reformatted README into markdown syntax and added more info

### Version 0.46
December 18, 2009

- First public release
- Included Orkut token
- Changed Google Analytics account

### Version 0.45
December 4, 2009

- Added simple Google Analytics tracking

### Version 0.44
December 1, 2009

- Adjusted/fixed some german translations
- Added author_link to gadget meta data
- Removed unneeded "external" css class

### Version 0.43
December 1, 2009

- Fixed l10n
- Added missing Serbian translations

### Version 0.42
November 30, 2009

- Gadget is localized to English (default), German, Spanish and Serbian
- Added affiliation
- Added default (English) screenshot
- Adjusted font-size, doc links are opened in a new window
- Gadget is now fully compliant with gadget specification
- Message extraction didn't work in this version

### Version 0.41
November 27, 2009

- Renamed gadget file to fig.xml

### Version 0.4
November 26, 2009

- Added Feature Documentation column for links to docs and tutorials for respective features
- Added table header
- Added atlassian-util feature
- We like short, catchy names so we've introduced one (FIG) and a corresponding gadget logo
- Code refactored


### Version 0.3

- Added check for google.blog and sharedmaps features.
- Adjusted html.
- Added info for unchecked features


### Version 0.2

- ALPHA version, Please test.


### Version 0.1
November 11, 2009

- The first and also a proof-of-concept version.


LICENSE
=======

FIG - Feature Inspector Gadget, find out what gadget features are supported by any gadget container.
Copyright (C) 2009 XING AG

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

