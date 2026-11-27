# Loon Shunt Rules (`.lsr`)

符合 Loon 最新分流规则规范（UTF-8 无 BOM、LF 换行、域名规则前置、IP 规则后置并统一追加 `no-resolve`）的个人云端分流规则库。

## 规则列表

| 规则文件 | 条数 | 推荐策略 | 说明 |
| :--- | :---: | :--- | :--- |
| `rules/Custom_Telegram.lsr` | 14 | `Telegram` | Telegram 核心域名与官方 DC IP 段 |
| `rules/Custom_Instagram.lsr` | 2 | `Instagram` | Instagram CDN 补充 |
| `rules/Custom_Grok.lsr` | 3 | `Grok` | Grok (xAI) 专属分流 |
| `rules/Custom_ChatGPT.lsr` | 7 | `ChatGPT` | ChatGPT / OpenAI / Sora 补充 |
| `rules/Custom_Claude.lsr` | 4 | `Claude` | Claude / Anthropic / Artifacts 补充 |
| `rules/Custom_Gemini.lsr` | 9 | `Gemini` | Gemini / AI Studio / Labs 补充 |
| `rules/Custom_AppleAI.lsr` | 7 | `AppleAI` | Apple Intelligence 专属分流 |
| `rules/Custom_Media.lsr` | 16 | `海外流媒体` | 自定义流媒体与视频站（需排在 `CN REGION` 之前） |
| `rules/Custom_JP.lsr` | 1 | `日本稳定策略` | 自定义日本线路域名 |
| `rules/Custom_Direct.lsr` | 46 | `DIRECT` | 自定义国内直连、音乐、图床及虚拟网段 |

## Loon `[Remote Rule]` 引用示例

```ini
[Remote Rule]
https://raw.githubusercontent.com/BeanJelly/loon-rules/main/rules/Custom_Telegram.lsr, policy=Telegram, tag=Telegram自定义, enabled=true
https://raw.githubusercontent.com/BeanJelly/loon-rules/main/rules/Custom_Instagram.lsr, policy=Instagram, tag=Instagram自定义, enabled=true
https://raw.githubusercontent.com/BeanJelly/loon-rules/main/rules/Custom_Grok.lsr, policy=Grok, tag=Grok, enabled=true
https://raw.githubusercontent.com/BeanJelly/loon-rules/main/rules/Custom_ChatGPT.lsr, policy=ChatGPT, tag=ChatGPT自定义, enabled=true
https://raw.githubusercontent.com/BeanJelly/loon-rules/main/rules/Custom_Claude.lsr, policy=Claude, tag=Claude自定义, enabled=true
https://raw.githubusercontent.com/BeanJelly/loon-rules/main/rules/Custom_Gemini.lsr, policy=Gemini, tag=Gemini自定义, enabled=true
https://raw.githubusercontent.com/BeanJelly/loon-rules/main/rules/Custom_JP.lsr, policy=日本稳定策略, tag=自定义日本, enabled=true
https://raw.githubusercontent.com/BeanJelly/loon-rules/main/rules/Custom_Media.lsr, policy=海外流媒体, tag=自定义视频流媒体, enabled=true
https://raw.githubusercontent.com/BeanJelly/loon-rules/main/rules/Custom_AppleAI.lsr, policy=AppleAI, tag=AppleAI, enabled=true
https://raw.githubusercontent.com/BeanJelly/loon-rules/main/rules/Custom_Direct.lsr, policy=DIRECT, tag=自定义直连, enabled=true
```
