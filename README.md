# pyfuze

## description

pyfuze makes your python script actually run anywhere.

## install

```bash
pip install pyfuze
```

## usage

```bash
pyfuze build t.py --python 3.8 --reqs requests,numpy
```

This command will generate `dist/t.zip` which contains:

- pyfuze.com
- .python-version (one line, "3.8")
- requirements.txt (two lines, "requests" and "numpy")
- t.py

`pyfuze.com` is an [actually portable executable](https://justine.lol/ape.html), so you can run it natively on Linux + Mac + Windows + FreeBSD + OpenBSD + NetBSD + BIOS on AMD64 and ARM64.

Notice: uv mainly supports macOS (Apple Silicon + x86_64), Linux (x86_64) and Windows (x86_64).

Executing `pyfuze.com` will result in:

- install uv in `./uv` folder
- install python in `./python` (version: `.python-version`)
- install dependencies in `requirements.txt`
- run python script
