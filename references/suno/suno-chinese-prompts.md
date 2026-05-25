# Suno Prompts for Chinese Music

Source: https://hookgenius.app/learn/suno-chinese-prompts/ (May 2026)

## Core Principles for Chinese Music in Suno

1. **Write lyrics in Chinese characters (汉字) in Custom Mode** — Suno handles characters better than pinyin for natural-sounding vocals
2. **Use specific genre tags** — "Mandopop" / "C-Pop" / "Chinese R&B" instead of generic "Chinese music"
3. **Name authentic instruments** — Suno recognizes guzheng, erhu, pipa, dizi by name
4. **Specify "singing in Mandarin Chinese"** in Style prompt to guide pronunciation
5. **Never rely on pinyin** — it loses tonal information and confuses the model

## Copy/Paste Prompt Templates

### Mandopop Ballad
```
Mandopop ballad, emotional male vocals singing in Mandarin Chinese, piano-driven, string arrangement, romantic, polished mix, slow tempo, heartfelt
```

### C-Pop Dance Hit
```
C-Pop, upbeat dance track, catchy female vocals in Mandarin, synth-heavy, EDM-influenced, polished production, energetic, radio-ready chorus
```

### Chinese R&B
```
Chinese R&B, smooth male vocals in Mandarin, neo-soul influence, lo-fi beats, atmospheric synths, midnight mood, intimate, modern
```

### Traditional Chinese Fusion
```
Chinese traditional fusion, guzheng, erhu, modern electronic production, ethereal female vocals in Mandarin, cinematic, atmospheric, East meets West
```

### Chinese Hip-Hop
```
Chinese hip-hop, aggressive male rap in Mandarin, trap beat, 808 bass, modern production, street energy, fast flow, hard-hitting
```

## Common Mistakes & Fixes

| Problem | Fix |
|---------|-----|
| Vocals sound like English with Chinese accent | Write lyrics in Chinese characters (汉字) in Custom Mode |
| Tones sound wrong | Break long phrases into shorter lines with clear punctuation |
| Music sounds generic, not Chinese | Add specific instruments: guzheng, erhu, bamboo flute + genre tags Mandopop/Chinese folk |
| Production too Western-sounding | Add "Chinese pop production, Asian pop influence, idol-group polish" |
| Vocals mispronouncing characters | Use `[Pronunciation: word = phonetic]` metatag for difficult characters |

## Language Support

- **Mandarin**: Best results. Write in simplified Chinese characters.
- **Cantonese**: Write in traditional Chinese characters used in Cantonese writing. Add "Cantonese vocals, Cantopop, Hong Kong pop" to style prompt.
- Both benefit from specifying the language explicitly in the Style field.

## Genre Tags That Work

- Mandopop / Mandopop Ballad
- C-Pop / C-Pop Dance
- Chinese R&B
- Chinese hip-hop
- Chinese folk ballad
- Chinese traditional fusion
- Cantopop / Hong Kong pop
