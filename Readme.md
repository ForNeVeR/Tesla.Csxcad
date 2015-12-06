Tesla.Csxcad [![Build status][appveyor-build-status]][appveyor-build] [![Status Umbra][status-umbra]][andivionian-status-classifier]
============

This is a part of the [Tesla project][tesla] responsible for parsing and
creating [CSXCAD][csxcad] files.

Build
-----

This project uses [Paket][paket] dependency manager. Before building the
project, you should download the dependencies. To install Paket and download the
dependencies, execute the following commands before opening the solution file:

    $ ./.paket/paket.bootstrapper.exe
    $ ./.paket/paket.exe install

CSX file generation
-------------------

Currently `Tesla.Csxcad` relies on the CSXCAD samples generated by the Octave /
MATLAB CSXCAD interface.

﻿To generate `Tools/CSX.xml`, install Octave and openEMS, and run the attached
script file. For example:

    $ cd Tools
    $ octave-cli Generate-CSX.m

Licensing
---------

Copyright © 2015 Friedrich von Never <friedrich@fornever.me>

This software may be at the user's choice used under the terms of:
- WTFPL (see `WTFPL.md` for details) [![WTFPL][wtfpl-badge]][wtfpl]
- MIT (see `MIT.md` for details)

[andivionian-status-classifier]: https://github.com/ForNeVeR/andivionian-status-classifier
[appveyor-build]: https://ci.appveyor.com/project/ForNeVeR/tesla-csxcad/branch/develop
[csxcad]: https://github.com/thliebig/CSXCAD
[paket]: https://fsprojects.github.io/Paket/index.html
[tesla]: https://github.com/ForNeVeR/Tesla
[wtfpl]: http://www.wtfpl.net/

[appveyor-build-status]: https://ci.appveyor.com/api/projects/status/hg2hjvmhwmiwf7q9/branch/develop?svg=true
[status-umbra]: https://img.shields.io/badge/status-umbra-red.svg
[wtfpl-badge]: http://www.wtfpl.net/wp-content/uploads/2012/12/wtfpl-badge-2.png
