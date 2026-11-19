# omnic-bucket

Scoop bucket for [omnic](https://github.com/push-rock/omnic) — content-aware
compression CLI. Every file is classified (~1 ms) and routed to the best codec
automatically; archives get per-file random access and corruption isolation.

## Install

```powershell
scoop bucket add omnic https://github.com/push-rock/omnic-bucket
scoop install omnic
```

Then:

```
omnic pack <dir> -o out.omnic      # classify + compress a whole tree
omnic unpack out.omnic             # extract (parallel writers)
omnic c file.txt                   # single stream, codec picked for you
```

## Update

`scoop update omnic` — the manifest tracks GitHub releases
(`checkver`/`autoupdate` are wired).
