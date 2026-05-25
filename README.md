# lyrics-composition

AI 歌词创作与音乐风格标签生成 Skill，专为 [opencode](https://opencode.ai) 设计。输出可直接用于 Suno、MiniMax 等 AI 音乐平台。

## 核心能力

- **作词**：中文/英文歌词创作，支持 8 种语言质感手法、12 种文学修辞、6 大创作原型、完整人称视角体系
- **自动风格推导**：写完歌词后，从歌词内容自动匹配 Genre / Mood / Instruments / Vocal / BPM / Key，生成 Suno/MiniMax 可直接使用的 Style/Tags 字段
- **共鸣机制**：特异性悖论、隐瞒的艺术、脆弱不对称、不解决的问题——让歌词从"写对了"变成"被记住了"
- **体裁覆盖**：抒情 Ballad、民谣叙事、独立摇滚、说唱、古风、内心独白、实验/氛围
- **专项支持**：唐恬式传承主题写作、方文山式炼字技巧、说唱押韵高密度写作
- **参考资源**：Suno Field Guide、工业级中文 Style 模板、Metatags 完整参考

## 快速开始

### 前置要求

- [opencode](https://opencode.ai) CLI 已安装并可用

### 将 Skill 添加到 opencode

方法一：使用配置文件

```jsonc
// opencode.jsonc
{
  "skills": [
    {
      "name": "lyrics-composition",
      "path": "/path/to/this/project/SKILL.md"
    }
  ]
}
```

方法二：放置在 opencode 默认 skills 目录

```bash
# macOS / Linux
ln -s /path/to/this/project ~/.config/opencode/skills/lyrics-composition
```

方法三：在对话中引用

```
/claude < /path/to/SKILL.md
```

Skill 加载后，当用户提到"写歌词""作词""填词""Suno 歌词"或描述一个主题想写成歌时，opencode 会自动调用此 skill。

## 项目结构

```
lyrics-composition/
├── SKILL.md                            # 核心 Skill 定义（980 行）
├── .opencode/
│   └── skills/lyrics-composition/
│       └── references/                 # 示例输出
│           ├── example-friendship-anthem.md
│           └── example-friendship-anthem-2.md
├── references/
│   └── suno/                           # Suno 参考手册
│       ├── suno-field-guide.md         # 社区 Suno Field Guide
│       ├── suno-industrial-handbook.md # 中文工业级制作手册
│       ├── suno-chinese-prompts.md     # 中文音乐专属模板
│       ├── blake-crosley-guide.md      # Metatags 参考
│       └── README.md                   # 参考源说明
└── README.md                           # 本文件
```

### 主要文件

| 文件 | 说明 |
|------|------|
| `SKILL.md` | 核心 Skill。包含创作原型系统、语言质感手法、押韵法则、POV 体系、Style 自动推导、工作流程等 |
| `references/suno/` | Suno 平台参考手册。构造 Style/Tags 时的深度参考，仅在需要工业级风格控制时读取 |
| `.opencode/skills/lyrics-composition/references/` | 示例歌词输出，展示 Skill 的完整输出格式和手法分析 |

## 用法示例

触发词：`写一首歌`、`写歌词`、`作词`、`填词`、`Suno 歌词`

```
用户：写一首关于友情的炸裂摇滚
助手：生成包含 -- STYLE/TAGS -- 和 -- LYRICS -- 的完整输出
```

Skill 的输出分为两部分：
- **STYLE/TAGS**：7 元素公式 Genre, Mood, Instruments, Vocal, Production, BPM, Key + Exclude
- **LYRICS**：带结构标签（Intro/Verse/Chorus/Bridge/Outro）和情绪标注的歌词文本

## 创作原型

Skill 内置 6 大创作原型，无需指定作词人即可匹配风格：

| 原型 | 核心来源 | 最佳场景 |
|------|---------|---------|
| 沉思者 | 林夕 + Leonard Cohen | 失恋、遗憾、深夜、领悟 |
| 说书人 | 黄伟文 + Bob Dylan | 叙事、社会议题、凡人传奇 |
| 水墨画师 | 方文山 + 周耀辉 | 古风、东方美学、氛围感 |
| 平凡英雄 | 唐恬 + Joni Mitchell | 传承、励志、家国主题 |
| 街头诗人 | 宋冬野 + 李志 + 赵雷 | 城市叙事、底层视角、怀旧 |
| 日记作者 | Taylor Swift + 李宗盛 | 分手回忆、个人故事、自我解剖 |

## 参考资源

- [opencode](https://opencode.ai) — AI 编程助手 CLI
- [Suno](https://suno.com) — AI 音乐生成平台
- [MiniMax](https://minimaxi.com) — AI 音乐生成平台

## License

MIT
