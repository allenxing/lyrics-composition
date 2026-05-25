# lyrics-composition

AI 歌词创作与音乐风格标签生成 Skill。输出可直接用于 Suno、MiniMax 等 AI 音乐平台。

## 使用方式

```bash
git clone git@github.com:allenxing/lyrics-composition.git
```

将 `SKILL.md` 的内容粘贴到你的 AI 项目知识库或系统提示词中。如果你是 opencode 用户，项目已内置 `.opencode/` 配置，clone 后自动生效。

## 核心能力

- **作词**：中文/英文歌词创作，支持 8 种语言质感手法、12 种文学修辞、6 大创作原型、完整人称视角体系
- **自动风格推导**：从歌词内容自动匹配 Genre / Mood / Instruments / Vocal / BPM / Key，生成 Suno/MiniMax 可直接使用的 Style/Tags 字段
- **共鸣机制**：特异性悖论、隐瞒的艺术、脆弱不对称、不解决的问题
- **体裁覆盖**：抒情 Ballad、民谣叙事、独立摇滚、说唱、古风、内心独白、实验/氛围
- **专项支持**：唐恬式传承主题写作、方文山式炼字技巧、说唱押韵高密度写作

## 项目结构

```
lyrics-composition/
├── SKILL.md                            # 核心 Skill 定义（唯一入口）
├── .opencode/skills/lyrics-composition/
│   └── references/                     # 示例输出
│       ├── example-friendship-anthem.md
│       └── example-friendship-anthem-2.md
├── references/
│   └── suno/                           # Suno 参考手册
│       ├── suno-field-guide.md
│       ├── suno-industrial-handbook.md
│       ├── suno-chinese-prompts.md
│       ├── blake-crosley-guide.md
│       └── README.md
└── README.md
```

## License

MIT
