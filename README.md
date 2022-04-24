# HDRCompare

Example Powershell [mpv][] command line:

```powershell
mpv `
    --lavfi-complex="$((Get-Content -Path .\hdr-compare.lavfi) -notlike '#*')" `
    --vf=format=colormatrix=bt.2020-ncl:colorlevels=limited:primaries=bt.2020:gamma=pq `
    <PATH TO HDR FILE> --external-file=<PATH TO SDR FILE>
```

Note: at the time of writing mpv [doesn't output HDR metadata][mpv10129], so the
display's HDR tone mapping might be somewhat suboptimal.

[mpv]: https://mpv.io/manual/master/#miscellaneous
[mpv10129]: https://github.com/mpv-player/mpv/issues/10129
