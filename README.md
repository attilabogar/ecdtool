# ecdtool

Tool for Working with CUE+FLAC CD Images

[![Build Status][1]][2]
[![SonarCloud Status][3]][4]
[![Coverage Status][5]][6]

[1]: https://travis-ci.org/attilabogar/ecdtool.svg?branch=master
[2]: https://travis-ci.org/attilabogar/ecdtool
[3]: https://sonarcloud.io/api/project_badges/measure?project=attilabogar_ecdtool&metric=alert_status
[4]: https://sonarcloud.io/dashboard?id=attilabogar_ecdtool
[5]: https://codecov.io/gh/attilabogar/ecdtool/branch/master/graph/badge.svg
[6]: https://codecov.io/gh/attilabogar/ecdtool


## Use Cases

  - Rename i18n track names to ASCII
  - Export an eCD to a single cue+wav image (can be burned to CD-ROM w/ `cdrdao`)


## How to create an eCD?

  - [EAC](http://exactaudiocopy.de/)
  - [dBpoweramp](https://www.dbpoweramp.com/cd-ripper.htm) (optional)

### Setup Exact Audio Copy

  - Use FLAC compression during the initial EAC setup wizard
  - EAC -> EAC Options -> Filename -> Naming scheme: `%tracknr2% %title%`

### Create eCD

  Start EAC and select from the menu:
  - Action -> Create CUE Sheet -> Current Gap Settings
  - Action -> Copy Selected Tracks -> Compressed

  Optionally dBpoweramp may be used to copy the audio tracks in FLAC format

## eCD directory tree example:

```
Favourite Artist - 2015 - Debut Album:
├── 01 First Track.flac
├── 02 Second Track.flac
...
├── 12 Last Track.flac
├── folder.jpg
└── Debut Album.cue
```


## Building

  - `git clone https://github.com/attilabogar/ecdtool.git`
  - `cd ecdtool`
  - `mvn package`


## Running

  `java -jar target/ecdtool-0.4-SNAPSHOT-jar-with-dependencies.jar`


## Status

Prototype - Work in Progress


## TODO

  - drop unused functions
  - drop CueSheet/DCP  
  - add buttons:
    - export cue+wav
    - apply rename
    - load current filenames
    - auto-correct filenames
  - export i18n mappings
  - add tests
  - AccurateRip support?


## Contributors

  - Attila Bogár
  - Csaba Soti


## Credits

  - [open iconic](https://useiconic.com/open/)
  - [jFLAC](http://jflac.sourceforge.net/)


## License

    MIT License

    Copyright (c) 2015-2019 Attila Bogár

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all 
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE 
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE 
    SOFTWARE.

**NOTE**: This software depends on other packages that may be licensed under
different open source licenses.
