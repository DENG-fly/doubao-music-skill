# doubao-music-skill 🎵

> Claude Code 技能：为豆包、Suno 等 AI 音乐工具创作高质量中文歌词与风格提示词——押韵规则、段落标签、质量七原则，复制粘贴即可出歌。
>
> A Claude Code skill that crafts high-quality Chinese lyrics and style prompts for Doubao, Suno & AI music tools — rhyme rules, metatags, and pro prompt principles. Copy-paste ready.

## ✨ 这是什么

写 AI 音乐最痛的两件事：**歌词不像人写的**、**提示词像歌单不像配乐**。

这个 skill 让 Claude Code 变成你的「作词人 + 制作人」：你说一句想法，它输出**复制粘贴即可用**的两段成品——

1. **风格描述（prompt）**：按专业配乐逻辑写，不是标签堆砌
2. **中文歌词**：押韵、音节可控、带 `[段落]/[唱腔]` 标签、有记忆点

```
你：帮我写一首关于"末班车"的都市民谣
Claude：
━━━━━━━━━━━━━━━━━━━━
🎵 《末班车的窗》
━━━━━━━━━━━━━━━━━━━━
【风格描述】（贴到豆包"风格"框）
都市民谣，72 BPM，深夜收尾的疲惫与温柔。近场收音的暖木吉他…
【歌词】（贴到"自定义歌词"框）
[Intro]
[Verse 1]
…
```

## 📦 安装

```bash
git clone https://github.com/DENG-fly/doubao-music-skill.git
cp -r doubao-music-skill/doubao-music ~/.claude/skills/
```

Windows（PowerShell）：

```powershell
git clone https://github.com/DENG-fly/doubao-music-skill.git
Copy-Item -Recurse doubao-music-skill\doubao-music $env:USERPROFILE\.claude\skills\
```

安装后**无需配置**，在任意项目里说「写歌词」「做首歌」即可触发；也可手动 `/doubao-music`。

## 🚀 使用

| 说法 | 效果 |
|------|------|
| 帮我写一首关于____的歌 | 全流程：歌词 + 风格描述 |
| 来一首古风 / 说唱 / 氛围纯音乐 | 按曲风出成品 |
| 写歌词（已有曲风想法） | 只要歌词 |
| 再改改，副歌没记忆点 | 按症状定位修改 |

## 🗂️ 结构

```
doubao-music/
├── SKILL.md                     # 主流程：需求 → 构思 → 歌词 → prompt → 成品
└── references/
    ├── quality-principles.md    # 风格描述质量七原则（配乐逻辑、物理形容词、声音记忆点…）
    ├── chinese-lyrics.md        # 中文歌词规则（押韵-情绪对照、音节、意象、结构分工）
    ├── metatags.md              # 标签字典（段落/人声唱腔/音效/语气词）
    └── style-vocab.md           # 词库（曲风×BPM 对照、乐器物理形容词、人声公式）
```

## 💡 核心方法论（节选）

**风格描述**：配乐逻辑 > 歌单逻辑
- ❌ `lo-fi chill 温暖好听`
- ✅ `近场收音的毡音钢琴，鼓刷 1:30 才进，每段过门一声挂钟报时`

**歌词**：押韵跟随情绪开口度（a/ang 昂扬外放，i/ü 亲密低语），副歌第一句就是记忆点，主歌只写"事与物"不写"我很伤心"。

**标签**：段落/唱腔用 `[方括号]`，音效用 `[[双括号]]`，标签单独成行、正文中文、标签英文。

## 🙏 致谢

本 skill 融合并改编了以下项目的思路（内容已重写适配中文/豆包场景）：

- [LocalSymmetry/lofn](https://github.com/LocalSymmetry/lofn) — 专业级 prompt 工程原则（配乐逻辑、物理形容词等）
- [yingray/music-creator](https://github.com/yingray/music-creator) — skill 工作流结构与知识库组织
- [JeffGreen311/eve-agent-v2-unleashed](https://github.com/JeffGreen311/eve-agent-v2-unleashed) — 元标签体系参考

## 📄 License

[MIT](./LICENSE)
