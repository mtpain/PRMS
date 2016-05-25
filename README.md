PRMS
====

Github mirror of Precipitation Runoff Modeling System

**Official Website:**  http://wwwbrr.cr.usgs.gov/projects/SW_MoWS/PRMS.html

The Precipitation-Runoff Modeling System is a deterministic, distributed-parameter, physical process based modeling system developed to evaluate the response of various combinations of climate and land use on streamflow and general watershed hydrology.

## Build (Unix)

This fork of PRMS is primarliy meant to enhance the documentation for building
PRMS from source. If your GCC libraries include the `libgfortran.a`, then you
should be able to run

```bash
make -C prmsIV
```

from the root of this repository. Unlike the "Linux" instructions in
`compile_notes`, you do not have to customize any paths. This mirror has set up
relative paths so this specification is unnecessary.

If you would like to tag the architecture
you're building on, first run

```bash
export ARC='OSX'
```

for example.

The `make` command above will use whatever C compiler is set in the environment
variable `CC`. So if you'd like to use `gcc` that is not the one returned by
`$ which gcc`, run, for example if you've installed the Homebrew GCC that
includes gfortran and its libraries,

```bash
export CC=/usr/local/Cellar/gcc/5.3.0/bin/gcc-5
```

Of course, be sure to run this before running `make -C prmsIV`.
If the build succeeds, your executable will be in the `bin` directory:
`bin/prmsIV`.

### Windows Build

For more information on Windows builds, see `compile_notes` in this same
directory.


### Source Code
- Original Source Code
    - ftp://brrftp.cr.usgs.gov/pub/mows/software/prms/3.0.5/prms3.0.5_src.tar.gz
- Compilation Notes:
    - ftp://brrftp.cr.usgs.gov/pub/mows/software/prms/prmsCompilation.txt)
    - To build, change $MOWSDIR in .../prmsIV/makelist and .../mmf/trunk/Makefile to the top level of this repository, and run make from ../prmsIV.

### References
- [Bibliography](http://wwwbrr.cr.usgs.gov/projects/SW_MoWS/Bibliography.html)

*Software licence information and typical disclaimers can be found at the USGS project listed above.*
