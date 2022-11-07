# Cygwin で nkf を Windows 向けにビルドする

Cygwin 上でそのまま make すると `cygwin1.dll` に依存するバイナリになってしまうため，
`CC = x86_64-w64-mingw32-gcc` にて make してみた．

## 手順

- nkf-2.1.5 `https://osdn.net/projects/nkf/downloads/70406/nkf-2.1.5.tar.gz/` をダウンロード
- Makefile 書き換え
    `CC = x86_64-w64-mingw32-gcc`
- make

## 環境

Windows 10 21H2 + Cygwin

```sh
$ cygcheck -c cygwin
Cygwin Package Information
Package              Version        Status
cygwin               3.3.6-1        OK
```

```sh
$ x86_64-w64-mingw32-gcc --version
x86_64-w64-mingw32-gcc (GCC) 11.3.0
Copyright (C) 2021 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```
