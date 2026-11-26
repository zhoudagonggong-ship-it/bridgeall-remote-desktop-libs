# bridgeall-remote-desktop-libs

Native libraries used by the BridgeAll remote-desktop plugin to encode screen tiles as WebP.

## Files (tag `v1`, folder `v1/`)

| File | Size (bytes) | SHA-256 |
|---|---|---|
| `v1/libwebp.dll` | 628224 | `3ba13e7a725b742c04c8801a751304a9eed1b9d1df08cc0acec54fe6db25458c` |
| `v1/libsharpyuv.dll` | 143872 | `ef1c1858b07c370ce416343452ff9dbce15d3f6ad0c4266edf26b5e2b75ae1eb` |

`libwebp.dll` depends only on `libsharpyuv.dll` and `KERNEL32.dll` (static C runtime).

## Source and build

- Upstream: https://github.com/webmproject/libwebp
- Tag: `v1.6.0` (tag object `b7e29b9d75bd31422b00c2a446d49d7af06c328d`, commit `4fa21912338357f89e4fd51cf2368325b59e9bd9`)
- Built unmodified on Windows x64 with Visual Studio 2022 Build Tools, from a `vcvars64` environment:

```
nmake /f Makefile.vc CFG=release-dynamic RTLIBCFG=static OBJDIR=output
```

Only `libwebp.dll` and `libsharpyuv.dll` from `output\release-dynamic\x64\bin\` are published here.

## License (libwebp, BSD-3-Clause) — upstream `COPYING`

```
Copyright (c) 2010, Google Inc. All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are
met:

  * Redistributions of source code must retain the above copyright
    notice, this list of conditions and the following disclaimer.

  * Redistributions in binary form must reproduce the above copyright
    notice, this list of conditions and the following disclaimer in
    the documentation and/or other materials provided with the
    distribution.

  * Neither the name of Google nor the names of its contributors may
    be used to endorse or promote products derived from this software
    without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

```

## Additional IP rights grant — upstream `PATENTS`

```
Additional IP Rights Grant (Patents)
------------------------------------

"These implementations" means the copyrightable works that implement the WebM
codecs distributed by Google as part of the WebM Project.

Google hereby grants to you a perpetual, worldwide, non-exclusive, no-charge,
royalty-free, irrevocable (except as stated in this section) patent license to
make, have made, use, offer to sell, sell, import, transfer, and otherwise
run, modify and propagate the contents of these implementations of WebM, where
such license applies only to those patent claims, both currently owned by
Google and acquired in the future, licensable by Google that are necessarily
infringed by these implementations of WebM. This grant does not include claims
that would be infringed only as a consequence of further modification of these
implementations. If you or your agent or exclusive licensee institute or order
or agree to the institution of patent litigation or any other patent
enforcement activity against any entity (including a cross-claim or
counterclaim in a lawsuit) alleging that any of these implementations of WebM
or any code incorporated within any of these implementations of WebM
constitute direct or contributory patent infringement, or inducement of
patent infringement, then any patent rights granted to you under this License
for these implementations of WebM shall terminate as of the date such
litigation is filed.
```
