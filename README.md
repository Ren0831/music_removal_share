# music_removal_share

This repository is intended to be published via **GitHub Pages** and host listening samples.

## How to update samples + QR (from `music_removal-main`)

From the `music_removal-main` workspace root:

```bash
python -m pip install -r tools/requirements_publish.txt
python tools/publish_music_removal_share.py
```

If you want to replace the 5 stable audio files under `docs/audio/`:

```bash
python tools/publish_music_removal_share.py \
  --mixture "C:\path\to\mixture.wav" \
  --target "C:\path\to\target.wav" \
  --baseline "C:\path\to\baseline.wav" \
  --metricgan "C:\path\to\metricgan.wav" \
  --distill "C:\path\to\distill.wav"
```

This regenerates:
- `docs/index.html`
- `docs/qr/all_samples.png`

## Push

```bash
cd share_publish/music_removal_share
git status
git add -A
git commit -m "Update listening samples + QR"
git push origin main
```


