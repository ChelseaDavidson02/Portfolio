# Chelsea Davidson, robotics portfolio

Static page for GitHub Pages. No build step.

## Add the videos

Put one MP4 per project in `videos/`, with exactly these names:

| File | Project |
| --- | --- |
| `videos/polymander.mp4` | Amphibious self-righting (Polymander II) |
| `videos/crazyflie.mp4` | Autonomous Crazyflie drone |
| `videos/quadruped.mp4` | Quadruped locomotion |
| `videos/rmp.mp4` | Surface following with Riemannian motion policies |
| `videos/miniature.mp4` | Miniature robotics |

A slot shows "Video coming soon" until its file exists, so you can add them one at a time.

Use H.264 MP4 so every browser plays it. To shrink a clip to about 720p:

```
ffmpeg -i input.mov -vf scale=-2:720 -c:v libx264 -crf 26 -preset slow -c:a aac -b:a 96k -movflags +faststart output.mp4
```

GitHub rejects any single file over 100 MB and asks you to keep a repository under about 1 GB. Under 20 MB per clip is a good target.

## Publish on GitHub Pages

1. On GitHub, create a public repository named `<your-username>.github.io`.
2. Upload everything in this folder (`index.html`, `videos/`, `.nojekyll`, `README.md`).
3. Open Settings, then Pages. Under "Build and deployment", choose "Deploy from a branch", pick `main` and `/ (root)`, and save.
4. After a minute the site is live at `https://<your-username>.github.io`.

A repository with any other name works too. The site is then at `https://<your-username>.github.io/<repo-name>/`, and the relative video paths still work.

## Edit the text

Everything is in `index.html`. Each project is one `<article>`. Change the bullets, the spec list and the figure caption there.
