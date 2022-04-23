# HDRCompare

Example Powershell [mpv][] command line:

```powershell
mpv --lavfi-complex="$(Get-Content -Path .\hdr-compare.lavfi -Raw)" <PATH TO HDR FILE> <PATH TO SDR FILE>
```

[mpv]: https://mpv.io/manual/master/#miscellaneous
