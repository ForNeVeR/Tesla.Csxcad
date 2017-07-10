Umov.Csxcad [![Build status][appveyor-build-status]][appveyor-build] [![Status Ventis][status-ventis]][andivionian-status-classifier] [![Nuget Package][nuget-badge]][nuget-Umov-csxcad]
============

This is a part of the [Umov project][Umov] responsible for parsing and
creating [CSXCAD][csxcad] and [openEMS][open-ems] files.

Debug
-----
To debug the library source in Visual Studio using the PDB from the NuGet
package, you need to enable source server support [as stated in GitLink
manual][gitlink-manual].

Build
-----

This project uses [Paket][paket] dependency manager. Before opening the solution
or building the project, you should install Paket (or Paket bootstrapper) into
`.paket` directory and download the dependencies using the following commands:

    $ ./.paket/paket.bootstrapper.exe
    $ ./.paket/paket.exe restore

For convenience, there is a script `Scripts/Install.ps1` that will download
Paket bootstrapper and call these commands automatically.

Consult the script documentation to discover its parameters.

Package
-------

To build [Nuget][nuget] package for Umov, use the script `Scripts/Package.ps1`.
If you want to push this package to the Nuget feed, use
`Scripts/Push-Package.ps1`.

Sample XML generation
---------------------

Currently `Umov.Csxcad` relies on [CSXCAD][csxcad] and [openEMS][open-ems]
samples generated by [Octave][octave] / MATLAB openEMS interface with some
static additions. These samples are concatenated and stored in
`Tools/Sample.lxml` file (which is not a well-formed XML but an XML element list
for [`XMLProvider`][fsharp-data-xml-provider]).

Raw XML contents of `CSX.xml` and `openEMS.xml` are also used for the unit
tests.

To generate these sample files, install Octave and openEMS, and run the attached
script file. For example:

    $ cd Tools
    $ octave-cli Generate-XML.m

Licensing
---------

Copyright © 2015–2017 Friedrich von Never <friedrich@fornever.me>

This software may be at the user's choice used under the terms of:
- WTFPL (see `WTFPL.md` for details) [![WTFPL][wtfpl-badge]][wtfpl]
- MIT (see `MIT.md` for details)

[andivionian-status-classifier]: https://github.com/ForNeVeR/andivionian-status-classifier
[appveyor-build]: https://ci.appveyor.com/project/ForNeVeR/Umov-csxcad/branch/develop
[csxcad]: https://github.com/thliebig/CSXCAD
[fsharp-data-xml-provider]: http://fsharp.github.io/FSharp.Data/library/XmlProvider.html
[gitlink-manual]: https://github.com/GitTools/GitLink#gitlink
[nuget]: https://www.nuget.org/
[nuget-Umov-csxcad]: https://www.nuget.org/packages/Umov.Csxcad/
[octave]: https://www.gnu.org/software/octave/
[open-ems]: http://openems.de/
[paket]: https://fsprojects.github.io/Paket/index.html
[Umov]: https://github.com/ForNeVeR/Umov
[wtfpl]: http://www.wtfpl.net/

[appveyor-build-status]: https://ci.appveyor.com/api/projects/status/hg2hjvmhwmiwf7q9/branch/develop?svg=true
[nuget-badge]: https://img.shields.io/nuget/vpre/Umov.Csxcad.svg
[status-ventis]: https://img.shields.io/badge/status-ventis-yellow.svg
[wtfpl-badge]: http://www.wtfpl.net/wp-content/uploads/2012/12/wtfpl-badge-2.png
