# cityhash-c #

C99 translation of Geoff Pike's and Jyrki Alakuijala's CityHash.

**This hash is superseded by FarmHash (see
[farmhash-c](https://github.com/uxcn/farmhash-c))**

### some notes... ###

This version of CityHash is translated from the original code released via
[google code](https://code.google.com/p/cityhash) (1.1.1), and may differ from
[smhasher](https://github.com/aappleby/smhasher).  For rough performance
metrics, please see Reini Urban's [smhasher](https://github.com/rurban/smhasher)
fork.

The code is intended to be platform agnostic, excluding some compiler
intrinsics.  However, please note `byte swap` and `rotate right` are used in the
hashes and platform optimized versions are not included, which may compromise
performance.  Additionally, `byte swap` is necessary for big-endian
architectures.
