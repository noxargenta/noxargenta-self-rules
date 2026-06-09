# noxargenta-self-rules

自定义 Clash 分流规则，基于 Z-Siqi/Clash-for-Windows_Rule 体系。

## 规则列表

| 文件 | 用途 | 策略 |
|------|------|------|
| `Rule/AI-Studio` | Google AI Studio / Gemini API | 🤖 Google AI Studio |
| `Rule/Codeforces` | Codeforces 竞赛 | 🏆 Codeforces |
| `Rule/AtCoder` | AtCoder 竞赛 | 🏆 AtCoder |
| `Rule/China-Direct` | OJ 站点 + Kook（直连） | DIRECT |
| `Rule/Steam-Gaming` | Steam 联机 + 街霸 6 游戏流量 | 🎮 Steam 联机 |
| `Rule/Steam-Store` | Steam 商店 / 社区 | 🛍️ Steam 商店 |

## 使用方式

在 Clash 配置的 `rule-providers` 中添加：

```yaml
rule-providers:
  AI-Studio:
    type: http
    behavior: classical
    url: "https://raw.githubusercontent.com/noxargenta/noxargenta-self-rules/main/Rule/AI-Studio"
    path: ./ruleset/ai-studio.yaml
    interval: 86400
```

然后在 `rules` 中添加：

```yaml
- RULE-SET,AI-Studio,🤖 Google AI Studio
```
