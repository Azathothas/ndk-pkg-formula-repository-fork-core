
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
