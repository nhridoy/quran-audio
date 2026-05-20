# Quran Audio — Complete Corpus (1–114)

This is the root repository for the Quran Audio Corpus. It contains 19 submodules, one per surah range, covering all 114 surahs of the Holy Quran recited by 17 renowned reciters.

## Structure

Each submodule follows the pattern:

```
{range}/{surah_number}/{reciter}/{ayah_number}.mp3
```

Example: `1-2/2/ar.shaatree/255.mp3`

## Range Repositories

| Submodule | Surahs | Repository |
|-----------|--------|------------|
| `1-2` | 1, 2 | `git@personal:nhridoy/1-2.git` |
| `3-4` | 3, 4 | `git@personal:nhridoy/3-4.git` |
| `5-6` | 5, 6 | `git@personal:nhridoy/5-6.git` |
| `7-8` | 7, 8 | `git@personal:nhridoy/7-8.git` |
| `9-10` | 9, 10 | `git@personal:nhridoy/9-10.git` |
| `11-12` | 11, 12 | `git@personal:nhridoy/11-12.git` |
| `13-16` | 13–16 | `git@personal:nhridoy/13-16.git` |
| `17-19` | 17–19 | `git@personal:nhridoy/17-19.git` |
| `20-22` | 20–22 | `git@personal:nhridoy/20-22.git` |
| `23-25` | 23–25 | `git@personal:nhridoy/23-25.git` |
| `26-27` | 26, 27 | `git@personal:nhridoy/26-27.git` |
| `28-33` | 28–33 | `git@personal:nhridoy/28-33.git` |
| `34-37` | 34–37 | `git@personal:nhridoy/34-37.git` |
| `38-42` | 38–42 | `git@personal:nhridoy/38-42.git` |
| `43-50` | 43–50 | `git@personal:nhridoy/43-50.git` |
| `51-55` | 51–55 | `git@personal:nhridoy/51-55.git` |
| `56-70` | 56–70 | `git@personal:nhridoy/56-70.git` |
| `71-80` | 71–80 | `git@personal:nhridoy/71-80.git` |
| `81-114` | 81–114 | `git@personal:nhridoy/81-114.git` |

## Reciters (17)

ar.abdullahbasfar, ar.abdulsamad, ar.abdurrahmaansudais, ar.ahmedajamy, ar.alafasy, ar.aymanswoaid, ar.hanirifai, ar.hudhaify, ar.husary, ar.husarymujawwad, ar.ibrahimakhbar, ar.mahermuaiqly, ar.muhammadayyoub, ar.muhammadjibreel, ar.parhizgar, ar.saoodshuraym, ar.shaatree

## CDN Links

To access individual ayah files via CDN, replace `{range}`, `{surah_number}`, `{reciter}`, and `{ayah_number}` placeholders:

**jsDelivr (preferred):**
```
https://cdn.jsdelivr.net/gh/nhridoy/{range}@main/{surah_number}/{reciter}/{ayah_number}.mp3
```

**GitHub Raw:**
```
https://raw.githubusercontent.com/nhridoy/{range}/refs/heads/main/{surah_number}/{reciter}/{ayah_number}.mp3
```

**Statically:**
```
https://cdn.statically.io/gh/nhridoy/{range}@main/{surah_number}/{reciter}/{ayah_number}.mp3
```

## llms.txt

See [llms.txt](./llms.txt) for a machine-readable index.

## License

106,011 MP3 files. All recitations are the property of their respective reciters.
