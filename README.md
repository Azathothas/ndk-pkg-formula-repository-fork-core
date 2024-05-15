

---
This is a mirror of [@leleliu008](https://github.com/leleliu008)'s [ndk-pkg-formula-repository-official-core](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core)
> - Prettified text-only [**`metadata`**](https://github.com/Azathothas/ndk-pkg-formula-repository-fork-core/blob/main/ndk.pkgs) containing info for _all packages_ is available at: https://github.com/Azathothas/ndk-pkg-formula-repository-fork-core/blob/main/ndk.pkgs
> - Raw [**`metadata`**](https://github.com/Azathothas/ndk-pkg-formula-repository-fork-core/blob/main/pkgs.json) containing info for _all packages_ is available as [**`json`**](https://raw.githubusercontent.com/Azathothas/ndk-pkg-formula-repository-fork-core/main/pkgs.json) & [**`yaml`**](https://raw.githubusercontent.com/Azathothas/ndk-pkg-formula-repository-fork-core/main/pkgs.yaml)
> - Pre Compiled Binaries using [@leleliu008](https://github.com/leleliu008)'s [ndk-pkg](https://github.com/leleliu008/ndk-pkg) is also available at https://bin.ajam.dev/arm64_v8a_Android/ as a part of [Azathothas/Toolpacks](https://github.com/Azathothas/Toolpacks)
> ---
> - Tips on Parsing
> > - [JSON `jq`](https://github.com/Azathothas/ndk-pkg-formula-repository-fork-core/blob/main/pkgs.json)
> > ```bash
> > curl -qfsSL "https://raw.githubusercontent.com/Azathothas/ndk-pkg-formula-repository-fork-core/main/pkgs.json" \
> > | jq -r '.[].$PROPERTY'
> > 
> > !# Example list only package names
> > curl -qfsSL "https://raw.githubusercontent.com/Azathothas/ndk-pkg-formula-repository-fork-core/main/pkgs.json" \
> > | jq -r '.[].pkgname'
> >
> > !# List all packages that contain the word `library` in their `.summary` in $PKG: $DESCRIPTION Format
> > curl -qfsSL "https://raw.githubusercontent.com/Azathothas/ndk-pkg-formula-repository-fork-core/main/pkgs.json" \
> > | jq -r '.[] | select(.summary | test("(?i)library")) | "\(.pkgname): \(.summary)"'
> > #To only print $PKGNAME: | jq -r '.[] | select(.summary | test("(?i)library")) | "\(.pkgname)"'
> > 
> > !# List all packages that DO NOT contain the word `library` in their `.summary` in $PKG: $DESCRIPTION Format
> > curl -qfsSL "https://raw.githubusercontent.com/Azathothas/ndk-pkg-formula-repository-fork-core/main/pkgs.json" \
> > | jq -r '.[] | select(.summary | test("library"; "i") | not) | "\(.pkgname): \(.summary)"'
> > #To only print $PKGNAME: | jq -r '.[] | select(.summary | test("library"; "i") | not) | "\(.pkgname)"'
> > ```
> > - [YAML `yq`](https://github.com/Azathothas/ndk-pkg-formula-repository-fork-core/blob/main/pkgs.yaml)
> > ```bash
> > curl -qfsSL "https://raw.githubusercontent.com/Azathothas/ndk-pkg-formula-repository-fork-core/main/pkgs.yaml" \
> > | yq eval '.[].$PROPERTY'
> > 
> > !# Example list only package names
> > curl -qfsSL "https://raw.githubusercontent.com/Azathothas/ndk-pkg-formula-repository-fork-core/main/pkgs.yaml" \
> > | yq eval '.[].pkgname'
> >
> > !# List all packages that contain the word `library` in their `.summary` in $PKG: $DESCRIPTION Format
> > curl -qfsSL "https://raw.githubusercontent.com/Azathothas/ndk-pkg-formula-repository-fork-core/main/pkgs.yaml" \
> > | yq eval '.[] | select(.summary | match("(?i)library")) | .pkgname + " : " + .summary'
> > #To only print $PKGNAME: | yq eval '.[] | select(.summary | match("(?i)library")) | .pkgname'
> >
> > !# List all packages that DO NOT contain the word `library` in their `.summary` in $PKG: $DESCRIPTION Format
> > curl -qfsSL "https://raw.githubusercontent.com/Azathothas/ndk-pkg-formula-repository-fork-core/main/pkgs.yaml" \
> > | yq eval '.[] | select(.summary | test("(?i)library") | not) | .pkgname + " : " + .summary'
> > #To only print $PKGNAME: | yq eval '.[] | select(.summary | test("(?i)library") | not) | .pkgname'
> > ```
> > ---
> > 

---
|Package | Version | Description | Homepage | Git |
|--------|---------|-------------|----------|-----|
| [**ARM_NEON_2_x86_SSE**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ARM_NEON_2_x86_SSE.yml) | 2024.05.15 | The platform independent header allowing to compile any C/C++ code containing ARM NEON intrinsic fun |  |  |
| [**aalib**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/aalib.yml) | 1.4rc5 | A portable ASCII art graphics library |  |  |
| [**abseil**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/abseil.yml) | 20240116.2 | C++ Common Libraries |  |  |
| [**acl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/acl.yml) | 2.3.2 | C library and utilities for Manipulating POSIX Access Control Lists |  |  |
| [**act**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/act.yml) | 0.2.62 | Run your GitHub Actions locally |  |  |
| [**actionlint**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/actionlint.yml) | 1.6.27 | Static checker for GitHub Actions workflow files |  |  |
| [**adig**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/adig.yml) | 1.28.1 | A command-line tool that allows you to perform DNS lookups from the command line |  |  |
| [**ag**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ag.yml) | 2.2.0 | A fast code-searching tool similar to ack |  |  |
| [**age**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/age.yml) | 1.1.1 | Simple, modern, secure file encryption |  |  |
| [**alass**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/alass.yml) | 2024.05.15 | Automatic Language-Agnostic Subtitle Synchronization |  |  |
| [**algernon**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/algernon.yml) | 1.16.0 | Pure Go web server with Lua, Markdown, HTTP/2 and template support |  |  |
| [**antibody**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/antibody.yml) | 6.1.1 | Shell plugin manager |  |  |
| [**aom**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/aom.yml) | 3.8.2 | Codec library for encoding and decoding AV1 video streams |  |  |
| [**apkeep**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/apkeep.yml) | 0.8.0 | A command-line tool for downloading APK files from various sources |  |  |
| [**aptly**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/aptly.yml) | 1.5.0 | Swiss army knife for Debian repository management |  |  |
| [**archiver**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/archiver.yml) | 3.5.1 | Cross-platform, multi-format archive utility |  |  |
| [**args**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/args.yml) | 6.3.0 | A simple header-only C++ argument parser library |  |  |
| [**aria2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/aria2.yml) | 1.37.0 | Download with resuming and segmented downloading |  |  |
| [**arping**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/arping.yml) | 2.24 | Utility to check whether MAC addresses are already taken on a LAN |  |  |
| [**attr**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/attr.yml) | 2.5.2 | C library and utilities for Manipulating Filesystem Extended Attributes |  |  |
| [**awk**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/awk.yml) | 20240422 | Text processing scripting language |  |  |
| [**axel**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/axel.yml) | 2.17.14 | A lightweight download accelerator |  |  |
| [**azcopy**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/azcopy.yml) | 10.24.0 | Azure Storage data transfer utility |  |  |
| [**b3sum**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/b3sum.yml) | 1.5.1 | A command line utility for calculating BLAKE3 hashes |  |  |
| [**base16**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/base16.yml) | 2024.05.15 | base16 encoder and decoder |  |  |
| [**base64**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/base64.yml) | 1.5 | Encode and decode base64 files |  |  |
| [**bash**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/bash.yml) | 5.2.21 | Bourne-Again SHell, a UNIX command interpreter |  |  |
| [**basis_universal**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/basis_universal.yml) | 1.16.4 | Basis Universal GPU texture codec command-line compression tool |  |  |
| [**bat**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/bat.yml) | 0.24.0 | Clone of cat(1) with syntax highlighting and Git integration |  |  |
| [**bc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/bc.yml) | 1.07.1 | Arbitrary precision numeric processing language |  |  |
| [**bcrypt**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/bcrypt.yml) | 1.1 | Cross platform file encryption utility using blowfish |  |  |
| [**berkeley-db**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/berkeley-db.yml) | 18.1.40 | A high-performance key/value database |  |  |
| [**bgrep**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/bgrep.yml) | 0.2 | Like grep but for binary strings |  |  |
| [**binaryen**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/binaryen.yml) | 117 | Compiler infrastructure and toolchain library for WebAssembly |  |  |
| [**bind**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/bind.yml) | 9.18.26 | Implementation of the DNS protocols |  |  |
| [**binocle**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/binocle.yml) | 0.3.0 | A graphical tool to visualize binary data |  |  |
| [**bison**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/bison.yml) | 3.8.2 | Yacc-compatible Parser generator |  |  |
| [**bk**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/bk.yml) | 0.6.0 | Terminal Epub reader |  |  |
| [**blockhash**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/blockhash.yml) | 0.3.3 | A perceptual image hash calculation tool based on algorithm descibed in Block Mean Value Based Image |  |  |
| [**boost**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/boost.yml) | 1.84.0 | A collection of portable C++ source libraries |  |  |
| [**boringssl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/boringssl.yml) | 2024.05.15 | A fork of OpenSSL that is designed to meet Google needs |  |  |
| [**boxes**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/boxes.yml) | 2.3.0 | Draw boxes around text |  |  |
| [**brook**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/brook.yml) | 20240404 | Cross-platform strong encryption and not detectable proxy. Zero-Configuration |  |  |
| [**broot**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/broot.yml) | 1.37.0 | New way to see and navigate directory trees |  |  |
| [**brotli**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/brotli.yml) | 1.1.0 | A generic-purpose lossless compression algorithm by Google |  |  |
| [**bsdtar**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/bsdtar.yml) | 3.7.4 | BSD tar |  |  |
| [**bullet**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/bullet.yml) | 3.25 | Physics SDK |  |  |
| [**byacc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/byacc.yml) | 20240109 | (Arguably) the best yacc variant |  |  |
| [**bzip2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/bzip2.yml) | 1.0.8 | Burrows–Wheeler-based data compression utilities with high compression ratio |  |  |
| [**caddy**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/caddy.yml) | 2.7.6 | A powerful, enterprise-ready, open source web server with automatic HTTPS |  |  |
| [**cairo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cairo.yml) | 1.18.0 | Vector graphics library with cross-device output support |  |  |
| [**cargo-c**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cargo-c.yml) | 0.9.31 | A helper program to build and install C-ABI compatible dynamic and static libraries |  |  |
| [**catch2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/catch2.yml) | 3.5.4 | Modern, C++-native, header-only, test framework |  |  |
| [**ccache**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ccache.yml) | 4.9.1 | Object-file caching compiler wrapper |  |  |
| [**cereal**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cereal.yml) | 1.3.2 | C++11 library for serialization |  |  |
| [**cfitsio**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cfitsio.yml) | 4.4.0 | C access to FITS data files with optional Fortran wrappers |  |  |
| [**cflow**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cflow.yml) | 1.7 | A command-line tool to generate call graphs from C code |  |  |
| [**cgal**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cgal.yml) | 5.6.1 | Computational Geometry Algorithms Library |  |  |
| [**cheat**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cheat.yml) | 4.4.2 | Create and view interactive cheat sheets for *nix commands |  |  |
| [**check**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/check.yml) | 0.15.2 | A unit testing framework for C |  |  |
| [**chezmoi**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/chezmoi.yml) | 2.48.0 | Manage your dotfiles across multiple diverse machines, securely |  |  |
| [**chinese-calendar**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/chinese-calendar.yml) | 2022.06.24 | chinese festival/jieqi algorithm |  |  |
| [**chisel**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/chisel.yml) | 1.9.1 | A fast TCP/UDP tunnel over HTTP |  |  |
| [**choose**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/choose.yml) | 1.3.1 | Human-friendly and fast alternative to cut and (sometimes) awk |  |  |
| [**cjson**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cjson.yml) | 1.7.17 | Ultralightweight JSON parser in ANSI C |  |  |
| [**cli11**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cli11.yml) | 2.4.1 | Simple and intuitive command-line parser for C++11 |  |  |
| [**clog**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/clog.yml) | 1.3.0 | Colorized pattern-matching log tail utility |  |  |
| [**cmake**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cmake.yml) | 3.29.2 | Cross-platform make |  |  |
| [**cmark**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cmark.yml) | 0.31.0 | The C reference implementation of CommonMark |  |  |
| [**cmatrix**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cmatrix.yml) | 2.0 | A command-line tool for producing a Matrix-style animation |  |  |
| [**cmocka**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cmocka.yml) | 1.1.7 | An elegant unit testing framework for C with support for mock objects |  |  |
| [**coreutils**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/coreutils.yml) | 9.5 | GNU File, Shell, and Text utilities |  |  |
| [**cotp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cotp.yml) | 1.5.0 | TOTP/HOTP authenticator app with import functionality |  |  |
| [**cpio**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cpio.yml) | 2.15 | Copies files into or out of a cpio or tar archive |  |  |
| [**cpprestsdk**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cpprestsdk.yml) | 2.10.19 | A C++ library for cloud-based client-server communication |  |  |
| [**cpptoml**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cpptoml.yml) | 0.1.1 | Header-only library for parsing TOML |  |  |
| [**cppunit**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cppunit.yml) | 1.15.1 | Unit testing framework for C++ |  |  |
| [**cpu_features**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cpu_features.yml) | 0.9.0 | Cross platform C99 library to get cpu features at runtime |  |  |
| [**cpuid**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cpuid.yml) | 2.2.7 | CPU feature identification for Go |  |  |
| [**cpuinfo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cpuinfo.yml) | 2024.05.15 | CPU INFOrmation library |  |  |
| [**croc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/croc.yml) | 9.6.15 | A command-line tool that allows you to easily and securely send files from one computer to another |  |  |
| [**crosstool-ng**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/crosstool-ng.yml) | 1.26.0 | A toolchain generator |  |  |
| [**crowbook**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/crowbook.yml) | 0.16.1 | A command-line tool to convert books written in Markdown to HTML, LaTeX/PDF and EPUB |  |  |
| [**ctop**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ctop.yml) | 0.7.7 | Top-like interface for container metrics |  |  |
| [**cue**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cue.yml) | 0.8.2 | Validate and define text-based and dynamic configuration |  |  |
| [**cunit**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cunit.yml) | 2.1.3 | Lightweight unit testing framework for C |  |  |
| [**curl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/curl.yml) | 8.7.1 | Get a file from an HTTP, HTTPS or FTP server |  |  |
| [**curlie**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/curlie.yml) | 1.7.2 | Power of curl, ease of use of httpie |  |  |
| [**cxxopts**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/cxxopts.yml) | 3.2.1 | A lightweight C++ command-line option parser |  |  |
| [**d2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/d2.yml) | 0.6.5 | A modern diagram scripting language that turns text to diagrams |  |  |
| [**d8**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/d8.yml) | 9.9.115.8 | A high-performance JavaScript and WebAssembly Engine powered by Google |  |  |
| [**darkhttpd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/darkhttpd.yml) | 1.16 | A small static web server without CGI |  |  |
| [**dasel**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dasel.yml) | 2.7.0 | JSON, YAML, TOML, XML, and CSV query and modification tool |  |  |
| [**dash**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dash.yml) | 0.5.12 | A POSIX-compliant implementation of /bin/sh that aims to be as small as possible |  |  |
| [**dav1d**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dav1d.yml) | 1.4.1 | AV1 decoder targeted to be small and fast |  |  |
| [**delta**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/delta.yml) | 0.17.0 | Syntax-highlighting pager for git and diff output |  |  |
| [**diffutils**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/diffutils.yml) | 3.10 | A package of several programs related to finding differences between files |  |  |
| [**dns2tcp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dns2tcp.yml) | 0.5.2 | TCP over DNS tunnel |  |  |
| [**dnslookup**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dnslookup.yml) | 1.10.0 | A simple command line utility to make DNS lookups to the specified server |  |  |
| [**dnsmap**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dnsmap.yml) | 0.36 | Passive DNS network mapper (a.k.a. subdomains bruteforcer) |  |  |
| [**dnsx**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dnsx.yml) | 1.2.1 | DNS query and resolution tool |  |  |
| [**dog**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dog.yml) | 0.1.0 | A command-line DNS client |  |  |
| [**doggo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/doggo.yml) | 0.5.7 | A command-line DNS client for humans |  |  |
| [**dos2unix**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dos2unix.yml) | 7.5.2 | Convert text between DOS, UNIX, and Mac formats |  |  |
| [**dot_static**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dot_static.yml) | 10.0.1 | A command-line tool for drawing graphs |  |  |
| [**double-conversion**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/double-conversion.yml) | 3.3.0 | Binary-decimal and decimal-binary routines for IEEE doubles |  |  |
| [**doxygen**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/doxygen.yml) | 1.10.0 | A command-line tool for generating documentation from annotated programming language source files |  |  |
| [**dua**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dua.yml) | 2.29.0 | A fast disk usage analyzer |  |  |
| [**duf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/duf.yml) | 0.8.1 | A better alternative to df(1) |  |  |
| [**dufs**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dufs.yml) | 0.40.0 | A file server that supports static serving, uploading, searching, accessing control, webdav... |  |  |
| [**duktape**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/duktape.yml) | 2.7.0 | An embeddable Javascript engine with a focus on portability and compact footprint |  |  |
| [**dust**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/dust.yml) | 1.0.0 | A more intuitive version of du(1) in rust |  |  |
| [**easyutils**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/easyutils.yml) | 2024.05.15 | A collections of easy to use command-line utilities |  |  |
| [**ed**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ed.yml) | 1.20.2 | Classic UNIX line editor |  |  |
| [**eigen3**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/eigen3.yml) | 3.4.0 | A C++ template library for linear algebra:matrices, vectors, numerical solvers, and related algorith |  |  |
| [**elvish**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/elvish.yml) | 0.20.1 | Friendly and expressive shell |  |  |
| [**epsilon**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/epsilon.yml) | 0.9.2 | Powerful wavelet image compressor |  |  |
| [**esbuild**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/esbuild.yml) | 0.20.2 | An extremely fast JavaScript bundler and minifier |  |  |
| [**ethereum**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ethereum.yml) | 1.13.14 | Go implementation of the Ethereum protocol |  |  |
| [**exa**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/exa.yml) | 0.10.1 | Modern replacement for ls(1) |  |  |
| [**exhale**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/exhale.yml) | 1.1.9 | Open source xHE-AAC encoder |  |  |
| [**exiv2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/exiv2.yml) | 0.28.2 | A command-line utility to read, write, delete and modify Exif, IPTC, XMP and ICC image metadata |  |  |
| [**eza**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/eza.yml) | 0.18.13 | Modern replacement for ls(1) |  |  |
| [**faac**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/faac.yml) | 1.30 | ISO AAC audio encoder |  |  |
| [**faad2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/faad2.yml) | 2.11.1 | ISO AAC audio decoder |  |  |
| [**fcp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fcp.yml) | 0.2.1 | A significantly faster alternative to the classic Unix cp(1) command |  |  |
| [**fd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fd.yml) | 9.0.0 | A simple, fast and user-friendly alternative to find(1) |  |  |
| [**fdk-aac**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fdk-aac.yml) | 2.0.3 | Standalone library of the Fraunhofer FDK AAC code from Android |  |  |
| [**fdroidcl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fdroidcl.yml) | 0.7.0 | F-Droid client |  |  |
| [**fff**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fff.yml) | 2.2 | A simple file manager written in bash |  |  |
| [**ffmpeg**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ffmpeg.yml) | 7.0 | A complete, cross-platform solution to record, convert and stream audio and video |  |  |
| [**figlet**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/figlet.yml) | 2.2.5 | Banner-like program prints strings as ASCII art |  |  |
| [**file**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/file.yml) | 5.45 | A command-line tool to determine file types |  |  |
| [**findent**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/findent.yml) | 4.3.2 | Indent and beautify Fortran sources and generate dependency information |  |  |
| [**findutils**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/findutils.yml) | 4.9.0 | A package of several programs related to finding files |  |  |
| [**fish**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fish.yml) | 3.7.1 | User-friendly command-line shell for UNIX-like operating systems |  |  |
| [**flac**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/flac.yml) | 1.4.3 | Free lossless audio codec |  |  |
| [**flatc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/flatc.yml) | 24.3.25 | An efficient cross platform serialization library for C++ |  |  |
| [**flex**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/flex.yml) | 2.6.4 | The Fast Lexical Analyzer, generates Scanners (tokenizers) |  |  |
| [**flock**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/flock.yml) | 0.4.0 | flock(1) locks files |  |  |
| [**fmt**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fmt.yml) | 10.2.1 | An open-source C/C++ library for formatting that provides a fast and safe alternative to C stdio and |  |  |
| [**fontconfig**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fontconfig.yml) | 2.15.0 | XML-based font configuration tools |  |  |
| [**fortune**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fortune.yml) | 3.18.0 | A command-line tool for displaying a random quotation |  |  |
| [**fp16**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fp16.yml) | 2024.05.15 | A header-only C/C++ library for conversion to/from half-precision floating point formats |  |  |
| [**freexl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/freexl.yml) | 2.0.0 | An open source library to extract data from Excel .xls files |  |  |
| [**fribidi**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fribidi.yml) | 1.0.13 | Implementation of the Unicode BiDi algorithm |  |  |
| [**fselect**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fselect.yml) | 0.8.5 | Find files with SQL-like queries |  |  |
| [**fsmon**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fsmon.yml) | 1.8.4 | Filesystem monitor with fanotify and inotify backends |  |  |
| [**fswatch**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fswatch.yml) | 1.17.1 | Monitor a directory for changes and run a shell command |  |  |
| [**fxdiv**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fxdiv.yml) | 2024.05.15 | A header-only library for division via fixed-point multiplication by inverse |  |  |
| [**fzf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fzf.yml) | 0.50.0 | A command-line fuzzy finder written in Go |  |  |
| [**fzy**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/fzy.yml) | 1.0 | A fast, simple fuzzy text selector with an advanced scoring algorithm |  |  |
| [**garble**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/garble.yml) | 0.12.1 | Obfuscate Go builds |  |  |
| [**gawk**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gawk.yml) | 5.3.0 | GNU awk utility |  |  |
| [**gbt**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gbt.yml) | 2.0.0 | Highly configurable prompt builder for Bash and ZSH written in Go |  |  |
| [**gd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gd.yml) | 2.3.3 | Graphics library to dynamically manipulate images |  |  |
| [**gdbm**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gdbm.yml) | 1.23 | GNU database manager |  |  |
| [**gdk-pixbuf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gdk-pixbuf.yml) | 2.42.10 | Toolkit for image loading and pixel buffer manipulation |  |  |
| [**gdu**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gdu.yml) | 5.27.0 | A pretty fast disk usage analyzer with console interface written in Go |  |  |
| [**geographiclib**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/geographiclib.yml) | r2.2 | C++ geography library |  |  |
| [**geos**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/geos.yml) | 3.12.1 | Geometry Engine |  |  |
| [**germanium**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/germanium.yml) | 1.2.2 | Generate image from source code |  |  |
| [**gettext**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gettext.yml) | 0.22.5 | GNU internationalization (i18n) and localization (l10n) library |  |  |
| [**gettext-dev**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gettext-dev.yml) | 0.22.5 | GNU internationalization (i18n) and localization (l10n) library |  |  |
| [**gettext-tools**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gettext-tools.yml) | 0.22.5 | GNU internationalization (i18n) and localization (l10n) library |  |  |
| [**gflags**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gflags.yml) | 2.2.2 | A C++ library for processing command-line flags |  |  |
| [**gh**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gh.yml) | 2.48.0 | A command-line interface that brings github.com functionality to your terminal |  |  |
| [**ghostscript**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ghostscript.yml) | 10.03.0 | Interpreter for PostScript and PDF |  |  |
| [**giflib**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/giflib.yml) | 5.2.1 | Library and utilities for processing GIFs |  |  |
| [**gindent**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gindent.yml) | 2.2.13 | C code prettifier |  |  |
| [**git**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/git.yml) | 2.44.0 | A free and open source distributed version control system with speed and efficiency |  |  |
| [**git-cliff**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/git-cliff.yml) | 2.2.0 | A highly customizable Changelog Generator that follows Conventional Commit specifications |  |  |
| [**git-lfs**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/git-lfs.yml) | 3.5.1 | A git extension for versioning large files |  |  |
| [**gitui**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gitui.yml) | 0.26.1 | Blazing fast terminal-ui for git written in rust |  |  |
| [**gitwatch**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gitwatch.yml) | 0.2 | Watch a file or folder and automatically commit changes to a git repo easily |  |  |
| [**glib**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/glib.yml) | 2.78.0 | A general-purpose, portable utility library which provides many useful data types, macros, type conv |  |  |
| [**glib-tools**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/glib-tools.yml) | 2.80.0 | A collection of tools for glib |  |  |
| [**glog**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/glog.yml) | 0.6.0 | Application-level logging library |  |  |
| [**glow**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/glow.yml) | 1.5.1 | A terminal based markdown reader |  |  |
| [**glslang**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/glslang.yml) | 14.1.0 | OpenGL and OpenGL ES reference compiler for shading languages |  |  |
| [**gm4**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gm4.yml) | 1.4.19 | Macro processing language |  |  |
| [**gmake**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gmake.yml) | 4.4.1 | Utility for directing compilation |  |  |
| [**gn**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gn.yml) | 2024.05.15 | A meta-build system for generating build files for ninja |  |  |
| [**gnu-barcode**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gnu-barcode.yml) | 0.99 | Convert text strings to printed bars |  |  |
| [**gnu-which**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gnu-which.yml) | 2.21 | GNU implementation of which utility |  |  |
| [**gnupg**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gnupg.yml) | 2.4.5 | GNU Pretty Good Privacy (PGP) package |  |  |
| [**gnutls**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gnutls.yml) | 3.8.4 | GNU Transport Layer Security (TLS) Library |  |  |
| [**go-md2man**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/go-md2man.yml) | 2.0.4 | Converts markdown into roff (man pages) |  |  |
| [**go-tools**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/go-tools.yml) | 2023.1.3 | A state-of-the-art linter for the Go programming language |  |  |
| [**godu**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/godu.yml) | 1.3 | A simple utility to discover large files/folders |  |  |
| [**gogs**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gogs.yml) | 0.13.0 | Go git service |  |  |
| [**golang**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/golang.yml) | 1.22.2 | Open source programming language to build simple/reliable/efficient software |  |  |
| [**gomobile**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gomobile.yml) | 2024.05.15 | A tool for building and running mobile apps written in Go |  |  |
| [**google-benchmark**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/google-benchmark.yml) | 1.8.3 | A C++ library to benchmark code snippets, similar to unit tests |  |  |
| [**google-highway**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/google-highway.yml) | 1.0.3 | Performance-portable, length-agnostic SIMD with runtime dispatch |  |  |
| [**googletest**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/googletest.yml) | 1.14.0 | C++ Testing and Mocking Framework by Google |  |  |
| [**gopls**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gopls.yml) | 0.15.3 | Language server for the Go language |  |  |
| [**goreleaser**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/goreleaser.yml) | 1.25.1 | Deliver Go binaries as fast and easily as possible |  |  |
| [**gosh**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gosh.yml) | 3.4.1 | A shell parser, formatter, and interpreter with bash support written in golang |  |  |
| [**gotop**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gotop.yml) | 4.2.0 | Terminal based graphical activity monitor inspired by gtop and vtop |  |  |
| [**gotty**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gotty.yml) | 1.5.0 | A simple command-line tool to share your terminal as a web application |  |  |
| [**gox**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gox.yml) | 1.0.1 | Go cross compile tool |  |  |
| [**gperf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gperf.yml) | 3.1 | Perfect hash function generator |  |  |
| [**gperftools**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gperftools.yml) | 2.15 | A collection of a high-performance multi-threaded malloc() implementation, plus some pretty nifty pe |  |  |
| [**gping**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gping.yml) | 1.16.1 | Ping, but with a graph |  |  |
| [**gpsim**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gpsim.yml) | 0.32.1 | Simulator for Microchip PIC microcontrollers |  |  |
| [**gputils**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gputils.yml) | 1.5.2 | GNU PIC Utilities |  |  |
| [**graphicsmagick**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/graphicsmagick.yml) | 1.3.43 | Image processing tools collection |  |  |
| [**graphviz**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/graphviz.yml) | 11.0.0 | An open source graph visualization software |  |  |
| [**grep**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/grep.yml) | 3.11 | GNU grep, egrep and fgrep |  |  |
| [**grex**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/grex.yml) | 1.4.5 | A command-line tool for generating regular expressions from user-provided test cases |  |  |
| [**gron**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gron.yml) | 0.7.1 | Make JSON greppable |  |  |
| [**grpc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/grpc.yml) | 1.62.2 | A modern, open source, high-performance remote procedure call (RPC) framework |  |  |
| [**grpc-plugins**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/grpc-plugins.yml) | 1.62.2 | grpc plugins |  |  |
| [**gsed**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gsed.yml) | 4.9 | GNU implementation of the famous stream editor |  |  |
| [**gtar**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gtar.yml) | 1.35 | GNU version of the tar archiving utility |  |  |
| [**gzip**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/gzip.yml) | 1.13 | A popular data compression program developed by GNU |  |  |
| [**halibut**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/halibut.yml) | 1.3 | Yet another free document preparation system |  |  |
| [**helix**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/helix.yml) | 24.03 | A post-modern modal text editor |  |  |
| [**helm**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/helm.yml) | 3.14.4 | Kubernetes package manager |  |  |
| [**hexdump**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/hexdump.yml) | 20181215 | hexdump library and cli |  |  |
| [**hexyl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/hexyl.yml) | 0.14.0 | A simple hex viewer for the terminal |  |  |
| [**htop**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/htop.yml) | 3.3.0 | Improved top (interactive process viewer) |  |  |
| [**htslib**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/htslib.yml) | 1.20 | A C library for high-throughput sequencing data formats |  |  |
| [**httpx**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/httpx.yml) | 1.6.0 | Fast and multi-purpose HTTP toolkit |  |  |
| [**hugo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/hugo.yml) | 0.125.4 | A fast and flexible static site generator |  |  |
| [**hunspell**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/hunspell.yml) | 1.7.2 | A free spell checker and morphological analyzer |  |  |
| [**hurl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/hurl.yml) | 4.3.0 | Run and Test HTTP Requests with plain text and curl |  |  |
| [**hwloc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/hwloc.yml) | 2.10.0 | Portable abstraction of the hierarchical topology of modern architectures |  |  |
| [**hydroxide**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/hydroxide.yml) | 0.2.21 | A third-party, open-source ProtonMail CardDAV, IMAP and SMTP bridge |  |  |
| [**hyperfine**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/hyperfine.yml) | 1.18.0 | A command-line tool for benchmarking |  |  |
| [**icu4c**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/icu4c.yml) | 74.2 | C/C++ and Java libraries for Unicode and globalization |  |  |
| [**id3lib**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/id3lib.yml) | 3.8.3 | An open-source library for manipulating ID3v1 and ID3v2 tags |  |  |
| [**ideviceinstaller**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ideviceinstaller.yml) | 1.1.1 | A command-line tool to manage apps on iOS devices |  |  |
| [**imagemagick**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/imagemagick.yml) | 7.1.1.15 | Tools and libraries to manipulate images in many formats |  |  |
| [**imath**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/imath.yml) | 3.1.11 | Library of 2D and 3D vector, matrix, and math operations |  |  |
| [**imlib2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/imlib2.yml) | 1.12.2 | Image loading and rendering library |  |  |
| [**inih**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/inih.yml) | r58 | A simple .ini file parser in C |  |  |
| [**invoice**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/invoice.yml) | 0.1.0 | A invoice generator |  |  |
| [**isl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/isl.yml) | 0.26 | Integer Set Library for the polyhedral model |  |  |
| [**iw**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/iw.yml) | 6.7 | A powerful tool for managing and manipulating wireless devices |  |  |
| [**ixwebsocket**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ixwebsocket.yml) | 11.3.2 | WebSocket client and server, and HTTP client command-line tool |  |  |
| [**jasper**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/jasper.yml) | 4.2.3 | Library for manipulating JPEG-2000 images |  |  |
| [**jbig2dec**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/jbig2dec.yml) | 0.20 | JBIG2 decoder and library (for monochrome documents) |  |  |
| [**jfrog-cli**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/jfrog-cli.yml) | 2.56.0 | A command-line interface for Jfrog Artifactory and Bintray |  |  |
| [**jj**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/jj.yml) | 0.16.0 | A git-compatible distributed version control system |  |  |
| [**jpeg**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/jpeg.yml) | 9f | Image manipulation library |  |  |
| [**jq**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/jq.yml) | 1.7.1 | A lightweight and flexible command-line JSON processor |  |  |
| [**json-c**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/json-c.yml) | 0.17 | A JSON parser for C |  |  |
| [**json-glib**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/json-glib.yml) | 1.8.0 | Library for JSON, based on GLib |  |  |
| [**jsoncpp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/jsoncpp.yml) | 1.9.5 | A C++ library for interacting with JSON |  |  |
| [**jump**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/jump.yml) | 0.51.0 | Helps you navigate your file system faster by learning your habits |  |  |
| [**kcp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/kcp.yml) | 1.7 | A Fast and Reliable ARQ Protocol |  |  |
| [**kcptun**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/kcptun.yml) | 20240107 | Stable & Secure Tunnel based on KCP with N/M multiplexing and FEC |  |  |
| [**keybase**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/keybase.yml) | 6.0.1 | Key directory that maps social media identities to encryption keys |  |  |
| [**ko**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ko.yml) | 0.15.2 | A simple, fast container image builder for Go applications |  |  |
| [**krb5**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/krb5.yml) | 1.21.2 | Network authentication protocol |  |  |
| [**lame**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lame.yml) | 3.100 | A high quality MPEG Audio Layer III (MP3) encoder |  |  |
| [**lazygit**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lazygit.yml) | 0.41.0 | A simple terminal UI for git commands |  |  |
| [**lcms2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lcms2.yml) | 2.16 | Color management engine supporting ICC profiles |  |  |
| [**lcov**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lcov.yml) | 2.0 | Graphical front-end for GCC coverage testing tool - gcov |  |  |
| [**ldns**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ldns.yml) | 1.8.3 | DNS library written in C |  |  |
| [**leptonica**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/leptonica.yml) | 1.84.1 | Image processing and image analysis library |  |  |
| [**less**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/less.yml) | 643 | Pager program similar to more |  |  |
| [**lf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lf.yml) | r26 | Terminal file manager |  |  |
| [**libaec**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libaec.yml) | 1.1.3 | Adaptive Entropy Coding implementing Golomb-Rice algorithm |  |  |
| [**libaio**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libaio.yml) | 0.3.113 | Linux-native asynchronous I/O access library |  |  |
| [**libao**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libao.yml) | 1.2.2 | A cross-platform audio library |  |  |
| [**libarchive**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libarchive.yml) | 3.7.4 | Multi-format archive and compression library |  |  |
| [**libargp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libargp.yml) | 1.5.0 | Standalone version of arguments parsing functions from GLIBC |  |  |
| [**libasprintf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libasprintf.yml) | 0.22.5 | C-style formatted output in C++ |  |  |
| [**libass**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libass.yml) | 0.17.1 | Subtitle renderer for the ASS/SSA subtitle format |  |  |
| [**libassuan**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libassuan.yml) | 2.5.7 | Assuan IPC Library |  |  |
| [**libasync++**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libasync++.yml) | 1.1 | A lightweight concurrency framework for C++11 |  |  |
| [**libatomic_ops**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libatomic_ops.yml) | 7.8.2 | Implementations for atomic memory update operations |  |  |
| [**libavif**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libavif.yml) | 1.0.4 | Library for encoding and decoding .avif files |  |  |
| [**libb2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libb2.yml) | 0.98.1 | Secure hashing function |  |  |
| [**libb64**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libb64.yml) | 1.2.1 | Base64 encoding/decoding library |  |  |
| [**libbcrypt**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libbcrypt.yml) | 2024.05.15 | A password hashing method based on the Blowfish block cipher, provided via the crypt(3) and a reentr |  |  |
| [**libblake3**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libblake3.yml) | 1.5.1 | C implementations of the BLAKE3 cryptographic hash function |  |  |
| [**libbluray**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libbluray.yml) | 1.3.4 | Blu-Ray disc playback library for media players like VLC |  |  |
| [**libbthread**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libbthread.yml) | 0.2 | provide some missing posix threading functions for NDK |  |  |
| [**libburn**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libburn.yml) | 1.5.2 | Library for writing preformatted data onto optical media (CD, DVD and BD) |  |  |
| [**libbz2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libbz2.yml) | 1.0.8 | Burrows–Wheeler-based data compression library with high compression ratio |  |  |
| [**libcaca**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcaca.yml) | 0.99.beta20 | Convert pixel information into colored ASCII art |  |  |
| [**libcap**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcap.yml) | 2.69 | Linux Capability Library |  |  |
| [**libcap-ng**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcap-ng.yml) | 0.8.5 | Library making programming with POSIX capabilities easier than traditional libcap |  |  |
| [**libcares**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcares.yml) | 1.28.1 | Asynchronous DNS library |  |  |
| [**libcbor**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcbor.yml) | 0.11.0 | CBOR protocol implementation for C and others |  |  |
| [**libcddb**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcddb.yml) | 1.3.2 | CDDB server access library |  |  |
| [**libcdio**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcdio.yml) | 2.1.0 | Compact Disc Input and Control Library |  |  |
| [**libcerf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcerf.yml) | 2.4 | Numeric library for complex error functions |  |  |
| [**libcgif**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcgif.yml) | V0.3.0 | A fast and lightweight GIF encoder written in C |  |  |
| [**libcpuinfo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcpuinfo.yml) | 2024.05.15 | CPU INFOrmation library |  |  |
| [**libcrc32c**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcrc32c.yml) | 1.1.2 | Implementation of CRC32C with CPU-specific acceleration |  |  |
| [**libcroco**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcroco.yml) | 0.6.13 | CSS parsing and manipulation toolkit for GNOME |  |  |
| [**libcrypt**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcrypt.yml) | 1 | crypt(3) implementation |  |  |
| [**libcurl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libcurl.yml) | 8.7.1 | A free and easy-to-use client-side URL transfer library |  |  |
| [**libdatrie**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libdatrie.yml) | 0.2.13 | Double-Array Trie Library |  |  |
| [**libdav1d**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libdav1d.yml) | 1.4.1 | AV1 decoder targeted to be small and fast |  |  |
| [**libde265**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libde265.yml) | 1.0.15 | An open source implementation of the H.265 video codec |  |  |
| [**libdeflate**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libdeflate.yml) | 1.20 | Heavily optimized DEFLATE/zlib/gzip compression and decompression |  |  |
| [**libduktape**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libduktape.yml) | 2.7.0 | An embeddable Javascript engine with a focus on portability and compact footprint |  |  |
| [**libedit**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libedit.yml) | 3.1 | BSD-style licensed readline alternative |  |  |
| [**libeigen**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libeigen.yml) | 3.4.0 | C++ template library for linear algebra |  |  |
| [**libev**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libev.yml) | 4.33 | Asynchronous event library |  |  |
| [**libevent**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libevent.yml) | 2.1.12 | Asynchronous event library |  |  |
| [**libexecinfo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libexecinfo.yml) | 2024.05.15 | A quick-n-dirty BSD licensed clone of backtrace facility found in the GNU libc |  |  |
| [**libexhale**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libexhale.yml) | 1.1.9 | Open source xHE-AAC encoder |  |  |
| [**libexif**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libexif.yml) | 0.6.24 | EXIF parsing library |  |  |
| [**libexiv2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libexiv2.yml) | 0.28.2 | A C++ library and a command-line utility to read, write, delete and modify Exif, IPTC, XMP and ICC i |  |  |
| [**libexpat**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libexpat.yml) | 2.6.2 | XML 1.0 parser |  |  |
| [**libffi**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libffi.yml) | 3.4.6 | A portable Foreign Function Interface library |  |  |
| [**libfftw3**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libfftw3.yml) | 3.3.10 | C library for computing the Discrete Fourier Transform |  |  |
| [**libflac**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libflac.yml) | 1.4.3 | Free lossless audio codec |  |  |
| [**libflatbuffers**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libflatbuffers.yml) | 24.3.25 | An efficient cross platform serialization library for C++ |  |  |
| [**libfontconfig**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libfontconfig.yml) | 2.15.0 | XML-based font configuration library |  |  |
| [**libfreetype**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libfreetype.yml) | 2.13.2 | A C library to render fonts |  |  |
| [**libgcrypt**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libgcrypt.yml) | 1.10.3 | Cryptographic library based on the code from GnuPG |  |  |
| [**libgeotiff**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libgeotiff.yml) | 1.7.1 | Library and tools for dealing with GeoTIFF |  |  |
| [**libgetdomainname**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libgetdomainname.yml) | 1 | get NIS domain name |  |  |
| [**libgetdtablesize**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libgetdtablesize.yml) | 1 | get descriptor table size |  |  |
| [**libgetloadavg**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libgetloadavg.yml) | 1 | get system load averages |  |  |
| [**libgit2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libgit2.yml) | 1.7.2 | C library of Git core methods that is re-entrant and linkable |  |  |
| [**libglm**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libglm.yml) | 1.0.1 | C++ mathematics library for graphics software |  |  |
| [**libglob**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libglob.yml) | 2024.05.15 | glob(3) implementation |  |  |
| [**libgmp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libgmp.yml) | 6.3.0 | GNU multiple precision arithmetic library |  |  |
| [**libgpg-error**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libgpg-error.yml) | 1.48 | Common error values for all GnuPG components |  |  |
| [**libgraphene**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libgraphene.yml) | 1.10.8 | Thin layer of graphic data types |  |  |
| [**libgraphite2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libgraphite2.yml) | 1.3.14 | Smart font renderer for non-Roman scripts |  |  |
| [**libharfbuzz**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libharfbuzz.yml) | 8.4.0 | A text shaping engine. It primarily supports OpenType, but also Apple Advanced Typography |  |  |
| [**libheif**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libheif.yml) | 1.17.6 | ISO/IEC 23008-12:2017 HEIF file format decoder and encoder |  |  |
| [**libhiredis**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libhiredis.yml) | 1.2.0 | Minimalistic client for Redis |  |  |
| [**libiconv**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libiconv.yml) | 1.17 | charset conversion library |  |  |
| [**libidn**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libidn.yml) | 1.42 | International domain name library |  |  |
| [**libidn2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libidn2.yml) | 2.3.7 | International domain name library (IDNA2008, Punycode and TR46) |  |  |
| [**libilbc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libilbc.yml) | 3.0.4 | Packaged version of iLBC codec from the WebRTC project |  |  |
| [**libimagequant**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libimagequant.yml) | 4.3.1 | Palette quantization library extracted from pnquant2 |  |  |
| [**libimobiledevice**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libimobiledevice.yml) | 1.3.0 | A C library to communicate with iOS devices natively |  |  |
| [**libimobiledevice-glue**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libimobiledevice-glue.yml) | 1.2.0 | Library with common system API code for libimobiledevice projects |  |  |
| [**libintl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libintl.yml) | 0.22.5 | GNU internationalization (i18n) and localization (l10n) library |  |  |
| [**libintl-lite**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libintl-lite.yml) | 2024.05.15 | A simple (but less powerful) GNU gettext libintl replacement |  |  |
| [**libirecovery**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libirecovery.yml) | 1.2.0 | Library and utility to talk to iBoot/iBSS via USB |  |  |
| [**libisoburn**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libisoburn.yml) | 1.5.2 | Frontend for libraries libburn and libisofs |  |  |
| [**libisofs**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libisofs.yml) | 1.5.6.pl01 | Library to create an ISO-9660 filesystem with extensions like RockRidge or Joliet |  |  |
| [**libjansson**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libjansson.yml) | 2.14 | C library for encoding, decoding, and manipulating JSON |  |  |
| [**libjpeg-turbo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libjpeg-turbo.yml) | 3.0.2 | A high-performance JPEG image codec that uses SIMD instructions (MMX, SSE2, AVX2, Neon, AltiVec) to  |  |  |
| [**libjxl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libjxl.yml) | 0.10.2 | New file format for still image compression |  |  |
| [**libksba**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libksba.yml) | 1.6.6 | X.509 and CMS library |  |  |
| [**liblanginfo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/liblanginfo.yml) | 2024.05.15 | langinfo.h and its implementation from android ndk source code |  |  |
| [**libleveldb**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libleveldb.yml) | 1.23 | Key-value storage library with ordered mapping |  |  |
| [**liblinear**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/liblinear.yml) | 2.47 | Library for large linear classification |  |  |
| [**liblmdb**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/liblmdb.yml) | 0.9.32 | An extraordinarily fast, memory-efficient, memory-mapped, key-value database |  |  |
| [**liblqr**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/liblqr.yml) | 0.4.2 | C/C++ seam carving library |  |  |
| [**liblua**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/liblua.yml) | 5.4.6 | Powerful, lightweight programming language |  |  |
| [**liblz4**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/liblz4.yml) | 1.9.4 | Extremely Fast Compression algorithm |  |  |
| [**liblzma**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/liblzma.yml) | 5.4.6 | A free, general-purpose data compression with a high compression ratio |  |  |
| [**liblzo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/liblzo.yml) | 2.10 | Real-time data compression library |  |  |
| [**libmagic**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmagic.yml) | 5.45 | A C library to determine file types |  |  |
| [**libmaxminddb**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmaxminddb.yml) | 1.9.1 | A C library for the MaxMind DB file format |  |  |
| [**libmblen**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmblen.yml) | 1 | get number of bytes in a character |  |  |
| [**libmd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmd.yml) | 1.1.0 | library provides message digest functions found on BSD systems |  |  |
| [**libmediainfo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmediainfo.yml) | 24.04 | Unified display of technical and tag data for audio/video |  |  |
| [**libmesalink**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmesalink.yml) | 2024.05.15 | memory-safe and OpenSSL-compatible TLS library |  |  |
| [**libmetalink**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmetalink.yml) | 0.1.3 | A C library to parse Metalink XML files |  |  |
| [**libmhash**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmhash.yml) | 0.9.9.9 | A large number of hash algorithms |  |  |
| [**libmill**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmill.yml) | 2024.05.15 | Go-style concurrency in C |  |  |
| [**libminiz**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libminiz.yml) | 2.2.0 | implements the zlib (RFC 1950) and Deflate (RFC 1951) compressed data format specification standards |  |  |
| [**libminizip**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libminizip.yml) | 1.3.1 | C library for zip/unzip via zLib |  |  |
| [**libmnl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmnl.yml) | 1.0.5 | Minimalistic Netlink Library based Linux kernel interfaces |  |  |
| [**libmp3lame**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmp3lame.yml) | 3.100 | A high quality MPEG Audio Layer III (MP3) encoder |  |  |
| [**libmpc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmpc.yml) | 1.3.1 | A C library for the arithmetic of high precision complex numbers |  |  |
| [**libmpfr**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmpfr.yml) | 4.2.1 | C library for multiple-precision floating-point computations |  |  |
| [**libmpir**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libmpir.yml) | 3.0.0 | Multiple Precision Integers and Rationals (fork of GMP) |  |  |
| [**libnet**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libnet.yml) | 1.3 | C library for creating IP packets |  |  |
| [**libnghttp2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libnghttp2.yml) | 1.61.0 | HTTP/2 C Library |  |  |
| [**libnl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libnl.yml) | 3.9.0 | Netlink Library based Linux kernel interfaces |  |  |
| [**libnng**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libnng.yml) | 1.7.3 | Nanomsg-next-generation -- light-weight brokerless messaging |  |  |
| [**libobstack**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libobstack.yml) | 1.2.3 | A standalone library to implement glibc obstack |  |  |
| [**libogg**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libogg.yml) | 1.3.5 | Ogg Bitstream Library |  |  |
| [**libopenh264**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libopenh264.yml) | 2.4.1 | Open Source H.264 Codec |  |  |
| [**libopus**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libopus.yml) | 1.5.2 | Audio codec |  |  |
| [**libpcap**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libpcap.yml) | 1.10.4 | Packet(TCP/IP) Capture library |  |  |
| [**libpcre**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libpcre.yml) | 8.45 | Perl compatible regular expressions library |  |  |
| [**libpcre2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libpcre2.yml) | 10.43 | Perl compatible regular expressions library with a new API |  |  |
| [**libphonenumber**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libphonenumber.yml) | 8.13.35 | A C++ library for parsing, formatting, and validating international phone numbers |  |  |
| [**libpipeline**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libpipeline.yml) | 1.5.7 | Library for manipulating pipelines of subprocesses in a flexible and convenient way |  |  |
| [**libpixman**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libpixman.yml) | 0.42.2 | A low-level library for pixel manipulation |  |  |
| [**libplist**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libplist.yml) | 2.4.0 | A library to handle Apple Property List format in binary or XML |  |  |
| [**libpng**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libpng.yml) | 1.6.43 | Library for manipulating PNG images |  |  |
| [**libpng++**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libpng++.yml) | 0.2.10 | C++ wrapper for libpng library |  |  |
| [**libprotobuf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libprotobuf.yml) | 26.1 | Protocol Buffers(data interchange format) compiler and library developed by Google |  |  |
| [**libpsl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libpsl.yml) | 0.21.5 | C library for the Public Suffix List |  |  |
| [**libpugixml**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libpugixml.yml) | 1.14 | Light-weight C++ XML processing library |  |  |
| [**libqalculate**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libqalculate.yml) | 5.0.0 | Library for Qalculate! program |  |  |
| [**libqrencode**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libqrencode.yml) | 4.1.1 | A fast and compact QR Code encoding library |  |  |
| [**libquiche**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libquiche.yml) | 2024.05.15 | Savoury implementation of the QUIC transport protocol and HTTP/3 |  |  |
| [**libraqm**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libraqm.yml) | 0.10.1 | A library for complex text layout |  |  |
| [**librasterlite**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/librasterlite.yml) | 1.1g | An open source library to store and retrieve huge raster coverages |  |  |
| [**librav1e**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/librav1e.yml) | 0.7.1 | The fastest and safest AV1 video encoder |  |  |
| [**libraw**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libraw.yml) | 0.21.2 | Library for reading RAW files from digital photo cameras |  |  |
| [**libre**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libre.yml) | 3.11.0 | Toolkit library for asynchronous network I/O with protocol stacks |  |  |
| [**libre2c**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libre2c.yml) | 3.1 | Generate C-based recognizers from regular expressions |  |  |
| [**libressl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libressl.yml) | 3.9.1 | Version of the SSL/TLS protocol forked from OpenSSL |  |  |
| [**librtmpdump**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/librtmpdump.yml) | 2.4.20151223 | A C library for downloading RTMP streaming media |  |  |
| [**librttopo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/librttopo.yml) | 1.1.0 | RT Topology Library |  |  |
| [**libsamplerate**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libsamplerate.yml) | 0.2.2 | Library for sample rate conpackage set version of audio data |  |  |
| [**libsass**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libsass.yml) | 3.6.6 | A C/C++ implementation of a Sass compiler |  |  |
| [**libsigsegv**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libsigsegv.yml) | 2.14 | A library for handling page faults in user mode |  |  |
| [**libsmi**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libsmi.yml) | 0.5.0 | A library to Access SMI MIB Information |  |  |
| [**libsnappy**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libsnappy.yml) | 1.1.10 | Compression/decompression library aiming for high speed |  |  |
| [**libsndfile**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libsndfile.yml) | 1.2.2 | C library for files containing sampled sound |  |  |
| [**libsodium**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libsodium.yml) | 1.0.19 | A modern, portable, easy to use crypto library |  |  |
| [**libspatialite**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libspatialite.yml) | 5.1.0 | Adds spatial SQL capabilities to SQLite |  |  |
| [**libspectre**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libspectre.yml) | 0.2.12 | Small library for rendering Postscript documents |  |  |
| [**libspeex**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libspeex.yml) | 1.2.1 | Audio codec designed for speech |  |  |
| [**libspeexdsp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libspeexdsp.yml) | 1.2.1 | Speex audio processing library |  |  |
| [**libspng**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libspng.yml) | 0.7.4 | A C library for reading and writing PNG format files with a focus on security and ease of use. |  |  |
| [**libsqlite3**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libsqlite3.yml) | 3.45.3 | A small, fast, self-contained, high-reliability, full-featured, SQL database engine written in C |  |  |
| [**libsrtp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libsrtp.yml) | 2.4.2 | Implementation of the Secure Real-time Transport Protocol |  |  |
| [**libssh**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libssh.yml) | 0.10.6 | C library SSHv1/SSHv2 client and server protocols |  |  |
| [**libssh2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libssh2.yml) | 1.11.0 | C library implementing the SSH2 protocol |  |  |
| [**libstrchrnul**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libstrchrnul.yml) | 1 | returns a pointer to the first occurrence of the character c in the string s |  |  |
| [**libtasn1**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libtasn1.yml) | 4.19.0 | ASN.1 structure parser library |  |  |
| [**libtesseract**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libtesseract.yml) | 5.3.4 | OCR (Optical Character Recognition) engine |  |  |
| [**libtextstyle**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libtextstyle.yml) | 0.22.5 | A C library that provides an easy way to add styling to programs that produce output to a console or |  |  |
| [**libthai**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libthai.yml) | 0.1.28 | Thai language support library |  |  |
| [**libtheora**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libtheora.yml) | 1.1.1 | Open video compression format |  |  |
| [**libtiff**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libtiff.yml) | 4.6.0 | TIFF library |  |  |
| [**libtinyxml2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libtinyxml2.yml) | 10.0.0 | A simple, small, efficient, C++ XML parser library |  |  |
| [**libtirpc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libtirpc.yml) | 1.3.3 | Port of Sun Transport-Independent RPC library to Linux |  |  |
| [**libtool**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libtool.yml) | 2.4.7 | Generic library support script |  |  |
| [**libtorrent-rakshasa**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libtorrent-rakshasa.yml) | 0.13.8 | BitTorrent library with a focus on high performance |  |  |
| [**libtorrent-rasterbar**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libtorrent-rasterbar.yml) | 2.0.10 | An efficient feature complete C++ bittorrent implementation focusing on efficiency and scalability |  |  |
| [**libtwolame**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libtwolame.yml) | 0.4.0 | Optimized MPEG Audio Layer 2 (MP2) encoder |  |  |
| [**libunibreak**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libunibreak.yml) | 6.1 | line breaking and word breaking algorithms |  |  |
| [**libunistring**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libunistring.yml) | 1.2 | C library for manipulating Unicode strings |  |  |
| [**libunwind**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libunwind.yml) | 1.7.2 | A portable and efficient C library for determining the call-chain of a program |  |  |
| [**libupnp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libupnp.yml) | 1.14.18 | Portable UPnP development kit |  |  |
| [**libusb**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libusb.yml) | 1.0.27 | A C library that provides generic access to USB devices |  |  |
| [**libusbmuxd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libusbmuxd.yml) | 2.1.0 | USB multiplexor library for iOS devices |  |  |
| [**libusrsctp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libusrsctp.yml) | 0.9.5.0 | Portable SCTP userland stack |  |  |
| [**libuuid**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libuuid.yml) | 2.39.3 | DCE compatible Universally Unique Identifier library |  |  |
| [**libuv**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libuv.yml) | 1.46.0 | Multi-platform support library with a focus on asynchronous I/O |  |  |
| [**libvips**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libvips.yml) | 8.15.2 | A fast image processing library with low memory needs |  |  |
| [**libvmaf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libvmaf.yml) | 3.0.0 | Perceptual video quality assessment based on multi-method fusion |  |  |
| [**libvorbis**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libvorbis.yml) | 1.3.7 | Vorbis General Audio Compression Codec |  |  |
| [**libvpx**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libvpx.yml) | 1.13.1 | VP8/VP9 video codec |  |  |
| [**libwavpack**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libwavpack.yml) | 5.7.0 | Hybrid lossless audio compression |  |  |
| [**libwebm**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libwebm.yml) | 1.0.0.31 | WebM container |  |  |
| [**libwebp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libwebp.yml) | 1.3.2 | Image format providing lossless and lossy compression for web images |  |  |
| [**libwebsockets**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libwebsockets.yml) | 4.3.3 | A flexible, lightweight pure C library for implementing modern network protocols easily with a tiny  |  |  |
| [**libwordexp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libwordexp.yml) | 2024.05.15 | wordexp(3) implementation |  |  |
| [**libx264**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libx264.yml) | r3108 | A free library for encoding video streams into the H.264/MPEG-4 AVC compression format |  |  |
| [**libx265**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libx265.yml) | 3.6 | An open-source H.265/HEVC encoder |  |  |
| [**libxcrypt**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libxcrypt.yml) | 4.4.36 | Extended crypt library for descrypt, md5crypt, bcrypt, and others |  |  |
| [**libxml2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libxml2.yml) | 2.12.6 | GNOME XML library |  |  |
| [**libxslt**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libxslt.yml) | 1.1.39 | C XSLT library for GNOME |  |  |
| [**libxvid**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libxvid.yml) | 1.3.7 | A high-performance, high-quality MPEG-4 video library |  |  |
| [**libyaml**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libyaml.yml) | 0.2.5 | A C library for parsing and emitting YAML |  |  |
| [**libyuv**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libyuv.yml) | 1788 | C library includes YUV conversion and scaling functionality |  |  |
| [**libz**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libz.yml) | 1.3.1 | A general purpose data compression library |  |  |
| [**libz3**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libz3.yml) | 4.12.6 | High-performance theorem prover |  |  |
| [**libzen**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libzen.yml) | 0.4.41 | Unified display of technical and tag data for audio/video |  |  |
| [**libzim**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libzim.yml) | 9.2.0 | Reference implementation of the ZIM specification |  |  |
| [**libzip**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libzip.yml) | 1.10.1 | A C library for reading, creating, and modifying zip archives |  |  |
| [**libzlog**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libzlog.yml) | 1.2.17 | A reliable, high-performance, thread-safe, flexible, clear-model logging library written in pure C |  |  |
| [**libzmq**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libzmq.yml) | 4.3.5 | An open-source universal messaging library |  |  |
| [**libzstd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/libzstd.yml) | 1.5.6 | A real-time compression library with high compression ratios |  |  |
| [**lief**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lief.yml) | 2024.05.15 | Library to Instrument Executable Formats |  |  |
| [**lighttpd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lighttpd.yml) | 1.4.76 | A secure, fast, compliant, and very flexible web server that has been optimized for high-performance |  |  |
| [**livego**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/livego.yml) | 0.0.15 | live video streaming server in golang |  |  |
| [**llhttp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/llhttp.yml) | 6.0.6 | http_parser replacement |  |  |
| [**lmdb**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lmdb.yml) | 0.9.32 | An extraordinarily fast, memory-efficient, memory-mapped, key-value database |  |  |
| [**lnd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lnd.yml) | 0.15.0 | Lightning Network Daemon |  |  |
| [**lodepng**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lodepng.yml) | 2024.05.15 | PNG encoder and decoder in C and C++ |  |  |
| [**log4cplus**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/log4cplus.yml) | 2.1.1 | A simple-to-use, log4j-like logging framework for C++ |  |  |
| [**lolcat**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lolcat.yml) | 1.2 | Rainbows and unicorns in your console |  |  |
| [**lrzip**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lrzip.yml) | 0.651 | Compression program with a very high compression ratio |  |  |
| [**lsd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lsd.yml) | 1.1.2 | A rewrite of GNU ls with lots of added features like colors, icons, tree-view, more formatting optio |  |  |
| [**lsof**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lsof.yml) | 4.99.3 | A command-line tool to list open files |  |  |
| [**lua**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lua.yml) | 5.4.6 | Powerful, lightweight programming language |  |  |
| [**luajit**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/luajit.yml) | 2.1.0 | Just-In-Time Compiler (JIT) for the Lua programming language |  |  |
| [**luau**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/luau.yml) | 0.623 | A fast, small, safe, gradually typed embeddable scripting language derived from Lua |  |  |
| [**lunzip**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lunzip.yml) | 1.14 | Decompressor for lzip files |  |  |
| [**lychee**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lychee.yml) | 0.14.3 | A fast, async, resource-friendly link checker |  |  |
| [**lynx**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lynx.yml) | 2.8.9rel.1 | A text-based web browser |  |  |
| [**lz4**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lz4.yml) | 1.9.4 | Extremely Fast Compression algorithm |  |  |
| [**lzip**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lzip.yml) | 1.24.1 | LZMA-based compression program similar to gzip or bzip2 |  |  |
| [**lzlib**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lzlib.yml) | 1.14 | Data compression library |  |  |
| [**lzop**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/lzop.yml) | 1.04 | A file compressor |  |  |
| [**magic_enum**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/magic_enum.yml) | 0.9.5 | Static reflection for enums (to string, from string, iteration) for modern C++ |  |  |
| [**mbedtls**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mbedtls.yml) | 3.6.0 | Cryptographic and SSL/TLS library |  |  |
| [**mcfly**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mcfly.yml) | 0.8.4 | Fly through your shell history |  |  |
| [**md4c**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/md4c.yml) | 0.5.2 | A fast, SAX-like Markdown parser for C |  |  |
| [**mdbook**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mdbook.yml) | 0.4.37 | A command-line tool to create modern online books from Markdown files |  |  |
| [**mediainfo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mediainfo.yml) | 24.04 | A convenient unified display of the most relevant technical and tag data for video and audio files |  |  |
| [**mimalloc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mimalloc.yml) | 2.1.2 | Compact general purpose allocator |  |  |
| [**minisign**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/minisign.yml) | 0.11 | A dead simple tool to sign files and verify signatures |  |  |
| [**minizip-ng**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/minizip-ng.yml) | 4.0.5 | Zip file manipulation library with minizip 1.x compatibility layer |  |  |
| [**mm-wiki**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mm-wiki.yml) | 0.2.1 | wiki manage service |  |  |
| [**mold**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mold.yml) | 2.30.0 | Modern Linker |  |  |
| [**mosh**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mosh.yml) | 1.4.0 | Remote terminal application |  |  |
| [**mozjpeg**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mozjpeg.yml) | 4.1.5 | Improved JPEG encoder |  |  |
| [**mpdecimal**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mpdecimal.yml) | 4.0.0 | Library for decimal floating point arithmetic |  |  |
| [**mpg123**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mpg123.yml) | 1.32.6 | MP3 player |  |  |
| [**mruby@3.0.0**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mruby@3.0.0.yml) | 3.0.0 | A lightweight implementation of the Ruby language |  |  |
| [**mruby@3.2.0**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/mruby@3.2.0.yml) | 3.2.0 | A lightweight implementation of the Ruby language |  |  |
| [**msgpack-c**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/msgpack-c.yml) | 6.0.1 | Library for a binary-based efficient data interchange format |  |  |
| [**naabu**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/naabu.yml) | 2.3.0 | Fast port scanner |  |  |
| [**nano**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nano.yml) | 7.2 | Free (GNU) replacement for the Pico text editor |  |  |
| [**nanomsg**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nanomsg.yml) | 1.2 | Socket library in C |  |  |
| [**nap**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nap.yml) | 0.1.1 | A code snippet manager for your terminal |  |  |
| [**nasm**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nasm.yml) | 2.16.02 | Netwide Assembler (NASM) is an 80x86 assembler |  |  |
| [**navi**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/navi.yml) | 2.23.0 | Interactive cheatsheet tool for the command-line |  |  |
| [**ncdu**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ncdu.yml) | 1.16 | NCurses Disk Usage |  |  |
| [**ncurses**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ncurses.yml) | 6.4 | Text-based UI library |  |  |
| [**neofetch**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/neofetch.yml) | 7.1.0 | Fast, highly customisable system info script |  |  |
| [**netcat**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/netcat.yml) | 0.7.1 | GNU netcat is a GNU rewrite of the classic netcat (aka nc) utility for reading and writing data on T |  |  |
| [**nethogs**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nethogs.yml) | 0.8.7 | Net top tool grouping bandwidth per process |  |  |
| [**netpbm**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/netpbm.yml) | 10.86.40 | A toolkit for manipulation of graphic images, including conversion of images between a variety of di |  |  |
| [**nettle**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nettle.yml) | 3.9.1 | Low-level cryptographic library |  |  |
| [**nghttp2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nghttp2.yml) | 1.61.0 | HTTP/2 C Library |  |  |
| [**nghttp3**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nghttp3.yml) | 2024.05.15 | HTTP/3 library written in C |  |  |
| [**nginx**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nginx.yml) | 1.25.4 | HTTP(S) server and reverse proxy, and IMAP/POP3 proxy server |  |  |
| [**ngtcp2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ngtcp2.yml) | 2024.05.15 | QUIC library written in C |  |  |
| [**ninja**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ninja.yml) | 1.12.0 | A small build system with a focus on speed |  |  |
| [**nlohmann-json**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nlohmann-json.yml) | 3.11.3 | JSON for modern C++ |  |  |
| [**nnn**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nnn.yml) | 4.9 | Tiny, lightning fast, feature-packed file manager |  |  |
| [**npth**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/npth.yml) | 1.6 | New GNU portable threads library |  |  |
| [**nsh**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nsh.yml) | 0.4.2 | Fish-like, POSIX-compatible shell |  |  |
| [**ntbtls**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ntbtls.yml) | 0.3.2 | Not Too Bad TLS library |  |  |
| [**nuclei**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nuclei.yml) | 3.2.6 | HTTP/DNS scanner configurable via YAML templates |  |  |
| [**numactl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/numactl.yml) | 2.0.18 | NUMA support for Linux |  |  |
| [**nushell**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/nushell.yml) | 0.92.2 | A new type of shell |  |  |
| [**oat++**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/oat++.yml) | 1.3.0 | A light and powerful web framework for C++ |  |  |
| [**obfs4proxy**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/obfs4proxy.yml) | 0.0.14 | Pluggable transport proxy for Tor, implementing obfs4 |  |  |
| [**oboe**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/oboe.yml) | 1.8.1 | An easy-to-use, high-performance audio library for Android |  |  |
| [**oniguruma**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/oniguruma.yml) | 6.9.9 | Regular expressions library |  |  |
| [**openal-soft**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/openal-soft.yml) | 1.23.1 | Implementation of the OpenAL 3D audio API |  |  |
| [**openblas**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/openblas.yml) | 0.3.26 | Optimized BLAS library |  |  |
| [**opencolorio**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/opencolorio.yml) | 2.3.2 | Color management solution geared towards motion picture production |  |  |
| [**opencv**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/opencv.yml) | 4.9.0 | Open source computer vision library |  |  |
| [**openexr**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/openexr.yml) | 3.2.4 | High dynamic-range image file format |  |  |
| [**openjpeg**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/openjpeg.yml) | 2.5.2 | Library for JPEG-2000 image manipulation |  |  |
| [**openlibm**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/openlibm.yml) | 0.8.2 | High quality, portable, open source libm implementation |  |  |
| [**openmpi**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/openmpi.yml) | 4.1.6 | High performance message passing library |  |  |
| [**openssl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/openssl.yml) | 3.3.0 | Cryptography and SSL/TLS Toolkit |  |  |
| [**openssl-dev**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/openssl-dev.yml) | 3.3.0 | Cryptography and SSL/TLS Toolkit |  |  |
| [**openssl-fips**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/openssl-fips.yml) | 2.0.16 | Cryptography and SSL/TLS Toolkit |  |  |
| [**openssl@1.1**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/openssl@1.1.yml) | 1.1.1w | Cryptography and SSL/TLS Toolkit |  |  |
| [**p11-kit**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/p11-kit.yml) | 0.24.1 | Library to load and enumerate PKCS#11 modules |  |  |
| [**p7zip**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/p7zip.yml) | 17.05 | 7-Zip (high compression file archiver) implementation |  |  |
| [**packcc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/packcc.yml) | 2024.05.15 | A packrat parser generator for C |  |  |
| [**pango**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pango.yml) | 1.52.2 | Framework for layout and rendering of i18n text |  |  |
| [**patch**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/patch.yml) | 2.7.6 | Apply a diff file to an original |  |  |
| [**patchelf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/patchelf.yml) | 0.18.0 | A small utility to modify ELF files |  |  |
| [**pbzip2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pbzip2.yml) | 1.1.13 | Parallel bzip2 |  |  |
| [**pcapplusplus**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pcapplusplus.yml) | 23.09 | C++ network sniffing, packet parsing and crafting framework |  |  |
| [**pcre2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pcre2.yml) | 10.43 | Perl compatible regular expressions library with a new API |  |  |
| [**pdfium**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pdfium.yml) | 1 | PDF read/write library by Google |  |  |
| [**pget**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pget.yml) | 0.2.1 | The fastest file download client |  |  |
| [**physfs**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/physfs.yml) | 3.2.0 | Library to provide abstract access to various archives |  |  |
| [**pigz**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pigz.yml) | 2.8 | A parallel implementation of gzip for modern multi-processor, multi-core machines |  |  |
| [**pjsip**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pjsip.yml) | 2.11.1 | A C library for multimedia protocols such as SIP, SDP, RTP and more |  |  |
| [**pkg-config**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pkg-config.yml) | 0.29.2 | Manage compile and link flags for libraries |  |  |
| [**pkgconf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pkgconf.yml) | 2.1.1 | Reimplementation of pkg-config |  |  |
| [**plog**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/plog.yml) | 1.1.10 | A portable, simple and extensible logging library for C++ |  |  |
| [**plzip**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/plzip.yml) | 1.11 | A massively parallel (multi-threaded) implementation of lzip, fully compatible with lzip 1.4 or newe |  |  |
| [**png**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/png.yml) | 1.6.43 | Library for manipulating PNG images |  |  |
| [**pngcheck**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pngcheck.yml) | 3.0.3 | Print info and check PNG, JNG, and MNG files |  |  |
| [**pngquant**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pngquant.yml) | 3.0.3.crate | PNG image optimizing utility |  |  |
| [**pngsplit**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pngsplit.yml) | 3.0.3 | Print info and check PNG, JNG, and MNG files |  |  |
| [**poco**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/poco.yml) | all | C++ class libraries for building network and internet-based applications |  |  |
| [**popt**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/popt.yml) | 1.19 | Library like getopt(3) with a number of enhancements |  |  |
| [**ppkg**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ppkg.yml) | 2024.05.15 | A portable package manager for Unix-like systems |  |  |
| [**procs**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/procs.yml) | 0.14.5 | Modern replacement for ps written by Rust |  |  |
| [**progress**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/progress.yml) | 0.17 | Coreutils progress viewer |  |  |
| [**proj**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/proj.yml) | 9.4.0 | Cartographic Projections Library |  |  |
| [**proj7**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/proj7.yml) | 7.2.1 | Cartographic Projections Library |  |  |
| [**proot2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/proot2.yml) | 5.1.107 | A user-space implementation of chroot, mount --bind, and binfmt_misc |  |  |
| [**protobuf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/protobuf.yml) | 26.1 | Protocol Buffers(data interchange format) compiler and library developed by Google |  |  |
| [**psimd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/psimd.yml) | 2024.05.15 | Portable 128-bit SIMD intrinsics |  |  |
| [**pthreadpool**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pthreadpool.yml) | 2024.05.15 | A portable and efficient thread pool implementation |  |  |
| [**pup**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pup.yml) | 2024.05.15 | Parse HTML at the command-line |  |  |
| [**putty**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/putty.yml) | 0.81 | Implementation of Telnet and SSH |  |  |
| [**pybind11**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pybind11.yml) | 2.12.0 | Seamless operability between C++11 and Python |  |  |
| [**pystring**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/pystring.yml) | 1.1.4 | C++ functions matching the interface and behavior of python string methods with std::string |  |  |
| [**python3**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/python3.yml) | 3.11.7 | Interpreted, interactive, object-oriented programming language |  |  |
| [**q**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/q.yml) | 0.19.1 | A tiny command line DNS client with support for UDP, TCP, DoT, DoH, DoQ and ODoH |  |  |
| [**qpdf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/qpdf.yml) | 11.9.0 | a command-line tool and C++ library that performs content-preserving transformations on PDF files |  |  |
| [**qrencode**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/qrencode.yml) | 4.1.1 | QR Code generation |  |  |
| [**quickjs**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/quickjs.yml) | 2024.01.13 | A small and embeddable JavaScript engine |  |  |
| [**ragel**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ragel.yml) | 6.10 | State machine compiler |  |  |
| [**rang**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/rang.yml) | 3.2 | A Minimal, Header only Modern c++ library for terminal goodies |  |  |
| [**rapidjson**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/rapidjson.yml) | 1.1.0 | A fast JSON parser and generator for C++ with SAX and DOM style APIs |  |  |
| [**rav1e**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/rav1e.yml) | 0.7.1 | The fastest and safest AV1 video encoder |  |  |
| [**rclone**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/rclone.yml) | 1.66.0 | Rsync for cloud storage |  |  |
| [**re2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/re2.yml) | 20240401 | Alternative to backtracking PCRE-style regular expression engines |  |  |
| [**re2c**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/re2c.yml) | 3.1 | Generate C-based recognizers from regular expressions |  |  |
| [**readline**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/readline.yml) | 8.2.10 | Library for command-line editing |  |  |
| [**restic**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/restic.yml) | 0.16.4 | A fast, efficient and secure backup program |  |  |
| [**resvg**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/resvg.yml) | 0.41.0 | A command-line tool to convert SVG to PNG |  |  |
| [**rhash**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/rhash.yml) | 1.4.4 | Utility for computing and verifying hash sums of files |  |  |
| [**ripgrep**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ripgrep.yml) | 14.1.0 | A command-line tool for searching files for a regex pattern |  |  |
| [**ripgrep-all**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ripgrep-all.yml) | 0.10.6 | Wrapper around ripgrep that adds multiple rich file types |  |  |
| [**rlwrap**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/rlwrap.yml) | 0.46.1 | Readline wrapper, adds readline support to tools that lack it |  |  |
| [**rsass**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/rsass.yml) | 0.23.0 | Sass reimplemented in rust with nom |  |  |
| [**rsync**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/rsync.yml) | 3.3.0 | Utility that provides fast incremental file transfer |  |  |
| [**rtmpdump**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/rtmpdump.yml) | 2.4+20151223 | A command-line tool for downloading RTMP streaming media |  |  |
| [**rtorrent**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/rtorrent.yml) | 0.9.8 | Ncurses BitTorrent client based on libtorrent-rakshasa |  |  |
| [**ruff**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ruff.yml) | 0.4.2 | An extremely fast Python linter, written in Rust |  |  |
| [**rust-analyzer**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/rust-analyzer.yml) | 2024.01.29 | A Rust compiler front-end for IDEs |  |  |
| [**ruy**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ruy.yml) | 2024.05.15 | matrix multiplication library |  |  |
| [**sassc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/sassc.yml) | 3.6.2 | Wrapper around libsass that helps to create command-line apps |  |  |
| [**scc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/scc.yml) | 3.2.0 | Fast and accurate code counter with complexity and COCOMO estimates |  |  |
| [**sd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/sd.yml) | 1.0.0 | Intuitive find & replace CLI |  |  |
| [**sdl2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/sdl2.yml) | 2.30.2 | A cross-platform development library designed to provide low level access to audio, keyboard, mouse, |  |  |
| [**shaderc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/shaderc.yml) | 2024.0 | A collection of tools, libraries, and tests for Vulkan shader compilation |  |  |
| [**shc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/shc.yml) | 4.0.3 | Shell Script Compiler |  |  |
| [**shell2http**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/shell2http.yml) | 1.17.0 | A HTTP server to execute shell commands |  |  |
| [**shellharden**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/shellharden.yml) | 4.3.1 | A bash syntax highlighter that encourages/fixes variables quoting |  |  |
| [**shiori**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/shiori.yml) | 1.5.0 | Simple bookmark manager built with Go |  |  |
| [**silicon**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/silicon.yml) | 0.5.2 | A command-line tool to render your source code into a beautiful image |  |  |
| [**simdjson**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/simdjson.yml) | 3.9.1 | SIMD-accelerated C++ JSON parser |  |  |
| [**sjpeg**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/sjpeg.yml) | 2024.05.15 | simple jpeg encoder |  |  |
| [**skcms**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/skcms.yml) | 2024.05.15 | SkCMS |  |  |
| [**skia**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/skia.yml) | 1 | An open source 2D graphics library |  |  |
| [**sl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/sl.yml) | 5.02 | Prints a steam locomotive if you type sl instead of ls |  |  |
| [**soundtouch**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/soundtouch.yml) | 2.3.1 | Audio processing library |  |  |
| [**spdlog**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/spdlog.yml) | 1.13.0 | Super fast C++ logging library |  |  |
| [**speex**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/speex.yml) | 1.2.1 | Audio codec designed for speech |  |  |
| [**sqlite3**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/sqlite3.yml) | 3.45.3 | A small, fast, self-contained, high-reliability, full-featured, SQL database engine written in C |  |  |
| [**starship**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/starship.yml) | 1.18.2 | The minimal, blazing-fast, and infinitely customizable prompt for any shell |  |  |
| [**stwolame**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/stwolame.yml) | 0.4.0 | Optimized MPEG Audio Layer 2 (MP2) encoder |  |  |
| [**stylua**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/stylua.yml) | 0.20.0 | An opinionated Lua code formatter |  |  |
| [**subfinder**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/subfinder.yml) | 2.6.6 | Subdomain discovery tool |  |  |
| [**supervisord**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/supervisord.yml) | 0.7.3 | A go-lang supervisor implementation |  |  |
| [**suricata**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/suricata.yml) | 7.0.5 | Network IDS, IPS, and security monitoring engine |  |  |
| [**svn-lite**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/svn-lite.yml) | 1.09 | A minimalist svn client to checkout/update Subversion repositories |  |  |
| [**svt-av1**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/svt-av1.yml) | 2.0.0 | AV1 encoder |  |  |
| [**swig**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/swig.yml) | 4.2.1 | A command-line tool for generating scripting interfaces to C/C++ code |  |  |
| [**syncthing**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/syncthing.yml) | 1.27.6 | Open source continuous file synchronization application |  |  |
| [**sysinfo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/sysinfo.yml) | 2024.05.15 | A command-line tool to get your currently running system information |  |  |
| [**szip**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/szip.yml) | 2.1.1 | Implementation of extended-Rice lossless compression algorithm |  |  |
| [**taglib**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/taglib.yml) | 1.13.1 | A library for reading and editing the metadata of several popular audio formats |  |  |
| [**talloc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/talloc.yml) | 2.4.2 | Hierarchical, reference-counted memory pool with destructors |  |  |
| [**tarlz**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tarlz.yml) | 0.25 | A massively parallel (multi-threaded) combined implementation of the tar archiver and the lzip compr |  |  |
| [**tbb**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tbb.yml) | 2021.11.0 | Rich and complete approach to parallelism in C++ |  |  |
| [**tbox**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tbox.yml) | 1.7.5 | A glib-like multi-platform c library |  |  |
| [**tcl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tcl.yml) | 8.6.14 | Tool Command Language |  |  |
| [**tcpdump**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tcpdump.yml) | 4.99.4 | A command-line tool to analyze packet(TCP/IP) |  |  |
| [**tdu**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tdu.yml) | 1.36 | Top Disk Usage |  |  |
| [**tealdeer**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tealdeer.yml) | 1.6.1 | A very fast implementation of tldr in Rust |  |  |
| [**tectonic**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tectonic.yml) | 0.15.0 | Modernized, complete, self-contained TeX/LaTeX engine |  |  |
| [**tengo**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tengo.yml) | 2.17.0 | Fast script language for Go |  |  |
| [**tiff**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tiff.yml) | 4.6.0 | TIFF library and utilities |  |  |
| [**tig**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tig.yml) | 2.5.9 | Text interface for Git repositories |  |  |
| [**tlrc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tlrc.yml) | 1.9.1 | Official tldr client written in Rust |  |  |
| [**tmux**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tmux.yml) | 3.4 | Terminal multiplexer |  |  |
| [**tokei**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tokei.yml) | 12.1.2 | Program that allows you to count code, quickly |  |  |
| [**toml++**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/toml++.yml) | 3.4.0 | A header-only C++17 (or later) library for parsing TOML |  |  |
| [**toml11**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/toml11.yml) | 3.8.1 | A header-only C++11 (or later) library for parsing TOML |  |  |
| [**tree**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tree.yml) | 2.1.1 | Display directories as trees (with optional color/HTML output) |  |  |
| [**trietool**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/trietool.yml) | 0.2.13 | A command-line tool for manipulating double-array trie data |  |  |
| [**ttyd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ttyd.yml) | 1.7.7 | A simple command-line tool for sharing terminal over the web |  |  |
| [**ttygif**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ttygif.yml) | 1.6.0 | A command-line tool to convert a ttyrec file into gif files |  |  |
| [**ttyrec**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/ttyrec.yml) | 1.0.8 | Terminal interaction recorder and player |  |  |
| [**tweego**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/tweego.yml) | 2.1.1 | A free command line compiler for Twine/Twee story formats |  |  |
| [**typos**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/typos.yml) | 1.20.10 | A source code spell checker |  |  |
| [**uctags**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/uctags.yml) | 2024.05.15 | Maintained ctags implementation |  |  |
| [**unbound**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/unbound.yml) | 1.19.3 | Validating, recursive, caching DNS resolver |  |  |
| [**unrar**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/unrar.yml) | 6.0.2 | Extract, view, and test RAR archives |  |  |
| [**uppm**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/uppm.yml) | 2024.05.15 | Universal Prebuild Package Manager |  |  |
| [**uppm@0.15.2**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/uppm@0.15.2.yml) | 2024.05.15 | Universal Prebuild Package Manager |  |  |
| [**usbmuxd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/usbmuxd.yml) | 1.1.1 | A socket daemon to multiplex connections from and to iOS devices |  |  |
| [**utf8.h**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/utf8.h.yml) | 2024.05.15 | single header utf8 string functions for C and C++ |  |  |
| [**utf8proc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/utf8proc.yml) | 2.9.0 | A small, clean C library for processing UTF-8 Unicode data |  |  |
| [**utfcpp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/utfcpp.yml) | 4.0.5 | UTF-8 with C++ in a Portable Way |  |  |
| [**uthash**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/uthash.yml) | 2.3.0 | C macros for hash tables and more |  |  |
| [**util-linux**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/util-linux.yml) | 2.39.3 | A collection of Linux utilities |  |  |
| [**v8**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/v8.yml) | 9.9.115.8 | A high-performance JavaScript and WebAssembly Engine powered by Google |  |  |
| [**valijson**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/valijson.yml) | 1.0.2 | Header-only C++ library for JSON Schema validation |  |  |
| [**vegeta**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/vegeta.yml) | 12.11.1 | HTTP load testing tool and library |  |  |
| [**vim**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/vim.yml) | 9.1.0300 | Vi IMproved - enhanced vi editor |  |  |
| [**virustotal-cli**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/virustotal-cli.yml) | 1.0.0 | command-line interface for VirusTotal |  |  |
| [**vulkan-headers**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/vulkan-headers.yml) | 1.3.283 | Vulkan Header files and API registry |  |  |
| [**wabt**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/wabt.yml) | 1.0.34 | Web Assembly Binary Toolkit |  |  |
| [**wasm3**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/wasm3.yml) | 0.5.0 | High performance WebAssembly interpreter |  |  |
| [**wasmtime**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/wasmtime.yml) | 20.0.0 | Standalone JIT-style runtime for WebAssembly, using Cranelift |  |  |
| [**watchexec**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/watchexec.yml) | 1.25.1 | Execute commands when watched files change |  |  |
| [**wavpack**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/wavpack.yml) | 5.7.0 | Hybrid lossless audio compression |  |  |
| [**webhook**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/webhook.yml) | 2.8.1 | A HTTP server to execute shell commands |  |  |
| [**webp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/webp.yml) | 1.4.0 | Image format providing lossless and lossy compression for web images |  |  |
| [**webrtc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/webrtc.yml) | 1 | Real-Time Communication |  |  |
| [**websocketpp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/websocketpp.yml) | 0.8.2 | C++ websocket client/server library |  |  |
| [**wget**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/wget.yml) | 1.24.5 | A free, open-source, command-line tool that is used to download files from web servers using HTTP, H |  |  |
| [**whois**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/whois.yml) | 5.5.22 | Lookup tool for domain names and other internet resources |  |  |
| [**wolfssl**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/wolfssl.yml) | 5.7.0 | A lightweight, portable SSL library written in C |  |  |
| [**wuzz**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/wuzz.yml) | 0.5.0 | Interactive cli tool for HTTP inspection |  |  |
| [**x264**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/x264.yml) | r3108 | A free library for encoding video streams into the H.264/MPEG-4 AVC compression format |  |  |
| [**x265**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/x265.yml) | 3.6 | An open-source H.265/HEVC encoder |  |  |
| [**xapian**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/xapian.yml) | 1.4.25 | C++ search engine library |  |  |
| [**xh**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/xh.yml) | 0.22.0 | A friendly and fast tool for sending HTTP requests |  |  |
| [**xmake**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/xmake.yml) | 2.9.1 | A cross-platform build utility based on Lua |  |  |
| [**xmlutils**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/xmlutils.yml) | 2.12.6 | A collections of command-line utilities provided by libxml2 |  |  |
| [**xmlwf**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/xmlwf.yml) | 2.6.2 | XML 1.0 parser |  |  |
| [**xnnpack**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/xnnpack.yml) | 2024.05.15 | High-efficiency floating-point neural network inference operators for mobile, server, and web |  |  |
| [**xorriso**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/xorriso.yml) | 1.5.6 | ISO9660+RR manipulation tool |  |  |
| [**xpup**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/xpup.yml) | 2024.05.15 | A command line XML parsing tool |  |  |
| [**xsltproc**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/xsltproc.yml) | 1.1.39 | C XSLT library for GNOME |  |  |
| [**xxd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/xxd.yml) | 9.1.0300 | A command-line tool to create a hex dump of a given file or standard input |  |  |
| [**xxhash**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/xxhash.yml) | 0.8.2 | Extremely fast non-cryptographic hash algorithm |  |  |
| [**xz**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/xz.yml) | 5.4.6 | A free, general-purpose data compression with a high compression ratio |  |  |
| [**yaml-cpp**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/yaml-cpp.yml) | 0.8.0 | YAML parser and emitter written in C++ for YAML 1.2 spec |  |  |
| [**yasm**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/yasm.yml) | 1.3.0 | Yet another assembler, a complete reimplementation of NASM |  |  |
| [**youtubedr**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/youtubedr.yml) | 2.10.1 | A command-line tool to download videos from youtube.com |  |  |
| [**yq**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/yq.yml) | 4.43.1 | A lightweight and portable command-line YAML processor |  |  |
| [**yyjson**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/yyjson.yml) | 0.9.0 | A high performance JSON library written in ANSI C |  |  |
| [**zlib**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/zlib.yml) | 1.3.1 | A general purpose data compression library |  |  |
| [**zlib-ng**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/zlib-ng.yml) | 2.1.6 | Zlib replacement with optimizations for next generation systems |  |  |
| [**zola**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/zola.yml) | 0.18.0 | Fast static site generator in a single binary with everything built-in |  |  |
| [**zopfli**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/zopfli.yml) | 1.0.3 | New zlib (gzip, deflate) compatible compressor |  |  |
| [**zoxide**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/zoxide.yml) | 0.9.4 | A shell extension to navigate your filesystem faster |  |  |
| [**zsh**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/zsh.yml) | 5.9 | Z Shell |  |  |
| [**zstd**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/zstd.yml) | 1.5.6 | A real-time compression utility with high compression ratios |  |  |
| [**zsync**](https://github.com/leleliu008/ndk-pkg-formula-repository-official-core/blob/master/formula/zsync.yml) | 0.6.2 | A file transfer program |  |  |

---
