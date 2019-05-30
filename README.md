# ecdtool

Tool for Working with CUE+FLAC CD Images

[![Build Status][1]][2]
[![SonarCloud Status][3]][4]

[1]: https://travis-ci.org/attilabogar/ecdtool.svg?branch=master
[2]: https://travis-ci.org/attilabogar/ecdtool
[3]: https://sonarcloud.io/api/project_badges/measure?project=attilabogar_ecdtool&metric=alert_status
[4]: https://sonarcloud.io/dashboard?id=attilabogar_ecdtool


## Use Cases

  - Rename UTF-8 track names to ASCII file naming
  - Fix CD' pressing offset
  - Dump eCD into cue+wav, which can burned with cdrdao
    optionally balancing the cd burner's write offset

# How to create an eCD?

  - [EAC](http://exactaudiocopy.de/)
  - [dBpoweramp](https://www.dbpoweramp.com/cd-ripper.htm)

To create a cue sheet of an Audio CD, start EAC and select from the menu:
  - Action -> Create CUE Sheet -> Current Gap Settings

For the flac files use naming scheme: %tracknr2% %title%

Alternatively dump the flac files using dBpoweramp using the corresponding file
naming scheme.

## An sample eCD looks like:

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
