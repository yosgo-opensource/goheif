# GoHeif - A go gettable decoder/converter for HEIC based on libde265

## Install

- `heic2jpg` to convert HEIC files to JPG preserving exif

```bash
go get https://github.com/yosgo-opensource/goheif
```

- Tested

  - Mac OS X (High Sierra)
  - Linux (Ubuntu 16.04 / GCC 5.4)
  - Windows 7 64bit with TDM-GCC 32 (GCC 5.1) and golang 1.12 windows/386

- Code Sample

```
func main() {
	goheif.Decode(file)
}
```

## What is done

- Fixed MAX_PREFIX warning

- Changes make to @bradfitz's (https://github.com/bradfitz) golang heif parser

  - Some minor bugfixes
  - A few new box parsers, noteably 'iref' and 'hvcC'

- Include libde265's source code (SSE by default enabled) and a simple golang binding

- A Utility `heic2jpg` to illustrate the usage.

## License

- heif and libde265 are in their own licenses

- goheif.go, libde265 golang binding and the `heic2jpg` utility are in MIT license

## Credits

- heif parser by @bradfitz (https://github.com/go4org/go4/tree/master/media/heif)
- libde265 (https://github.com/strukturag/libde265)
- implementation learnt from libheif (https://github.com/strukturag/libheif)

## TODO

- Upstream the changes to heif?
