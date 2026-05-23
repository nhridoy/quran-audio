# AGENTS.md — Quran Audio Corpus

## Repository structure

Top-level dirs are surah ranges (e.g., `1-2`, `3-4`, … `81-114`). Each contains:

```
{range}/{surah_number}/{reciter}/{ayah_number}.mp3
```

Example: `1-2/2/ar.shaatree/255.mp3`

### 19 range directories

| Dir | Surahs | Dir | Surahs |
|-----|--------|-----|--------|
| `1-2` | 1, 2 | `3-4` | 3, 4 |
| `5-6` | 5, 6 | `7-8` | 7, 8 |
| `9-10` | 9, 10 | `11-12` | 11, 12 |
| `13-16` | 13–16 | `17-19` | 17–19 |
| `20-22` | 20–22 | `23-25` | 23–25 |
| `26-27` | 26, 27 | `28-33` | 28–33 |
| `34-37` | 34–37 | `38-42` | 38–42 |
| `43-50` | 43–50 | `51-55` | 51–55 |
| `56-70` | 56–70 | `71-80` | 71–80 |
| `81-114` | 81–114 | | |

### 17 reciters (100% coverage across all 114 surahs)

`ar.abdullahbasfar`, `ar.abdulsamad`, `ar.abdurrahmaansudais`, `ar.ahmedajamy`, `ar.alafasy`, `ar.aymanswoaid`, `ar.hanirifai`, `ar.hudhaify`, `ar.husary`, `ar.husarymujawwad`, `ar.ibrahimakhbar`, `ar.mahermuaiqly`, `ar.muhammadayyoub`, `ar.muhammadjibreel`, `ar.parhizgar`, `ar.saoodshuraym`, `ar.shaatree`

## Git workflow per range directory

```bash
git init
git add .
git config user.email "hridoyboss12@gmail.com"
git config gpg.format ssh
git config user.signingkey ~/.ssh/github_nhridoy
git commit -asm "added: {range}"          # e.g. "added: 1-2"
git branch -M main
git remote add origin git@personal:nhridoy/{range}.git
git push -u origin main
```

Then generate README.md and llms.txt with jsDelivr CDN links, add, commit (`git commit -asm "docs: add README and llms.txt"`), and push.

## README / llms.txt generation

Each range directory gets a README.md and llms.txt. Use this CDN link pattern (prefer jsDelivr):

```
https://cdn.jsdelivr.net/gh/nhridoy/{range}@{branch}/{surah_number}/{reciter}/{ayah_number}.mp3
https://raw.githubusercontent.com/nhridoy/{range}/refs/heads/{branch}/{surah_number}/{reciter}/{ayah_number}.mp3
https://cdn.statically.io/gh/nhridoy/{range}@{branch}/{surah_number}/{reciter}/{ayah_number}.mp3
```

List the surahs and reciters present in that range. Include a link to the llms.txt from README.md.

## Optional root super-repo

If creating a root repo (`quran-audio.git`) with submodules:

```bash
git init
git submodule add git@personal:nhridoy/1-2.git 1-2
# ... for each range
```

Then add README.md + llms.txt covering all ranges. Push to `git@personal:nhridoy/quran-audio.git`.

## SSH host config

Remote uses host alias `personal` (defined in `~/.ssh/config`), not `github.com` directly.

## No code, only audio

106,011 MP3 files, 0 other files. No build tools, tests, dependencies, or config files exist.
