# mov2images

code

mkdir -p frames

for f in *.[mM][oO][vV]; do
  base="$(basename "$f" | sed 's/\.[mM][oO][vV]$//')"
  ffmpeg -i "$f" -vf "fps=1,transpose=1" "frames/${base}_frame%d.jpg"
done