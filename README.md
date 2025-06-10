# mov2images

code

```
for f in *.[mM][oO][vV]; do
  base="$(basename "$f" | sed 's/\.[mM][oO][vV]$//')"
  ffmpeg -i "$f" -vf "fps=1,transpose=1" "frames/${base}_frame%d.jpg"
done
```

for larger files

```
git config --global http.postBuffer 524288000
```