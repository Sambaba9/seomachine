# Changelog

## v1.0.0 (2026-04-26)

> 初始发布 — SEO Machine Hermes Agent 适配版
> Initial release — SEO Machine Hermes Agent Adaptation

### 新增 | Added
- **微信二维码** `assets/wechat_qr.png` — README 底部添加扫码联系板块
- **CLI 工具** `bin/seomachine` — 7 个 Hermes Agent 可调用的 SEO 命令
  - `keywords` - 关键词研究 + 搜索意图分析
  - `write` - 生成 SEO 文章大纲
  - `analyze` - 页面 SEO 健康检查
  - `score` - 内容质量评分 (0-100)
  - `research` - 竞争对手研究
  - `cluster` - 主题集群策略
  - `audit` - 全面 SEO 审计
- **Python 分析模块** 24 个，包括 SEOQualityRater、ContentScorer、KeywordAnalyzer、SearchIntentAnalyzer 等
- **CLAUDE.md** Claude Code 工作空间配置（保留原项目生态）
- **.claude/commands/** 24 个 SEO 命令
- **.claude/agents/** 11 个专业 Agent 角色
- **context/** 11 个品牌/SEO 指南文件
- **10 个独立研究脚本**（竞品差距、SERP 分析、主题集群等）

### 适配 | Adapted
- 原始项目 [TheCraigHewitt/seomachine](https://github.com/TheCraigHewitt/seomachine) (MIT) → Hermes Agent 兼容
- 添加了中英双语 README.md 说明文档
- CLI 封装：所有模块可通过 `python3 bin/seomachine <command>` 调用

### 技术栈 | Tech Stack
- Python 3.11+
- scikit-learn, nltk, textstat, beautifulsoup4, lxml, pandas, numpy
- Playwright (可选的页面抓取)
- GA4 / Google Search Console / DataForSEO API 集成
- WordPress REST API 发布 (Yoast SEO)
