# SEO Machine 🚀

> 搜索引擎优化全流程工具 — 关键词研究 · 内容评分 · 搜索意图分析 · SERP 分析 · 竞争对手研究  
> Full-stack SEO toolkit — Keyword Research · Content Scoring · Search Intent · SERP Analysis · Competitor Research

[![GitHub Stars](https://img.shields.io/github/stars/Sambaba9/seomachine?style=flat-square)](https://github.com/Sambaba9/seomachine)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.11+-blue.svg?style=flat-square)](https://www.python.org/)

基于 **[TheCraigHewitt/seomachine](https://github.com/TheCraigHewitt/seomachine)** (6.7k ⭐, MIT) 开源项目适配，整合 Claude Code 工作空间 → Hermes Agent 兼容的 CLI 工具链。包含 24 个 Python 分析模块、10 个独立研究脚本、35+ Claude 命令/Agent 角色库。

Adapted from the open-source **TheCraigHewitt/seomachine** (6.7k ⭐, MIT). Integrates a Claude Code workspace into a Hermes Agent-compatible CLI toolkit with 24 Python analysis modules, 10 research scripts, and 35+ Claude commands/agent personas.

---

## 📋 目录 | Table of Contents

- [快速开始](#-快速开始--quick-start)
- [CLI 命令](#-cli-命令--commands)
- [Python 分析模块](#-python-分析模块--python-analysis-modules)
- [Claude 命令 & Agent 库](#-claude-命令--agent-库)
- [项目结构](#-项目结构--project-structure)
- [数据源集成](#-数据源集成--data-source-integration)
- [后续计划](#-后续计划--roadmap)

---

## 🚀 快速开始 | Quick Start

### 安装依赖 | Install Dependencies

```bash
# 克隆仓库 / Clone
git clone https://github.com/Sambaba9/seomachine.git
cd seomachine

# 安装依赖 / Install Python packages
pip install -r data_sources/requirements.txt
```

### CLI 使用 | CLI Usage

```bash
# 关键词研究与意图分析 / Keyword research & intent analysis
python3 bin/seomachine keywords "SEO优化"

# 生成 SEO 文章大纲 / Generate SEO article outline
python3 bin/seomachine write "亚马逊SEO优化指南"

# 内容质量评分（0-100）/ Content quality scoring
python3 bin/seomachine score path/to/article.md

# 列出所有命令 / List all commands
python3 bin/seomachine list-commands
```

### Claude Code 集成 | Claude Code Integration

```bash
# 按主题研究关键词和竞争对手 / Research keywords & competitors
/research "your topic"

# 创建 SEO 优化文章 / Create SEO-optimized article
/write "your topic"

# 优化已有内容 / Optimize existing content
/optimize path/to/article.md

# 分析已有页面 / Analyze existing page
/analyze-existing https://example.com/page

# 发布到 WordPress / Publish to WordPress
/publish-draft path/to/draft.md
```

---

## 🛠 CLI 命令 | Commands

| 命令 | 说明 (中文) | Description (English) |
|------|------------|----------------------|
| `keywords <topic>` | 关键词研究 + 搜索意图分析 | Keyword research & search intent analysis |
| `write <topic>` | 生成 SEO 文章大纲 | Generate SEO article outline |
| `analyze <url>` | 页面 SEO 健康检查 | Page SEO health audit |
| `score <file>` | 内容质量评分 (0-100) | Content quality scoring (0-100) |
| `research <topic>` | 竞争对手研究 | Competitor research |
| `cluster <topic>` | 主题集群策略 | Topic cluster strategy |
| `audit <file\|url>` | 全面 SEO 审计 | Comprehensive SEO audit |
| `list-commands` | 列出所有命令 | List all commands |

---

## 📦 Python 分析模块 | Python Analysis Modules

位于 `data_sources/modules/`，可直接在 Python 中导入使用：

| 模块 | 类 | 功能 (中文) | Function (English) |
|------|-----|-----------|-------------------|
| `seo_quality_rater` | `SEOQualityRater` | SEO 质量评分 (0-100)，25+ 检查项 | SEO quality rating, 25+ checks |
| `content_scorer` | `ContentScorer` | 5 维综合评分（人性化/具体性/结构/SEO/可读性） | 5-dimension composite scoring |
| `keyword_analyzer` | `KeywordAnalyzer` | 关键词密度/分布/TF-IDF 聚类 | Keyword density, distribution, clustering |
| `readability_scorer` | `ReadabilityScorer` | Flesch 可读性评分 + 句子节奏 | Flesch Reading Ease + sentence rhythm |
| `search_intent_analyzer` | `SearchIntentAnalyzer` | 搜索意图分类（信息/导航/交易/商业调查） | Search intent classification |
| `content_length_comparator` | `ContentLengthComparator` | 对比 TOP 10 SERP 内容长度 | Benchmark vs top 10 SERP results |
| `opportunity_scorer` | `OpportunityScorer` | 8 因子机会评分 | 8-factor opportunity scoring |
| `landing_page_scorer` | `LandingPageScorer` | 着陆页评分 | Landing page scoring |
| `article_planner` | `ArticlePlanner` | 文章结构规划 | Article structure planning |
| `competitor_gap_analyzer` | `CompetitorGapAnalyzer` | 竞争对手内容差距分析 | Competitor content gap analysis |
| `section_writer` | `SectionWriter` | 内容分段撰写 | Content section writing |
| `data_aggregator` | `DataAggregator` | 多数据源聚合 | Multi-source data aggregation |
| `cro_checker` | `CROChecker` | 转化率优化检查 | CRO (Conversion Rate Optimization) check |
| `cta_analyzer` | `CTAAnalyzer` | 行动号召分析 | Call-to-action analysis |
| `trust_signal_analyzer` | `TrustSignalAnalyzer` | 信任信号分析 | Trust signal analysis |
| `engagement_analyzer` | `EngagementAnalyzer` | 用户互动分析 | User engagement analysis |
| `content_scrubber` | `ContentScrubber` | 内容清洗 | Content scrubbing |
| `above_fold_analyzer` | `AboveFoldAnalyzer` | 首屏内容分析 | Above-fold content analysis |
| `social_research_aggregator` | `SocialResearchAggregator` | 社交媒体研究聚合 | Social media research aggregation |

### Python 代码示例 | Python Code Example

```python
import sys
sys.path.insert(0, 'data_sources/modules')

from seo_quality_rater import SEOQualityRater
from content_scorer import ContentScorer
from search_intent_analyzer import SearchIntentAnalyzer
from keyword_analyzer import KeywordAnalyzer

# 搜索意图分析 / Search intent analysis
intent = SearchIntentAnalyzer().analyze("SEO优化")
print(f"意图: {intent['primary_intent']}")  # informational

# SEO 质量评分 / SEO quality rating
rater = SEOQualityRater()
score = rater.rate(
    content="文章内容...",
    meta_title="文章标题",
    meta_description="文章描述",
    primary_keyword="关键词"
)

# 多维度内容评分 / Multi-dimension content scoring
scorer = ContentScorer()
result = scorer.score("文章内容...")
print(f"综合评分: {result['composite_score']}/100")
print(f"通过: {result['passed']}")
```

---

## 📁 Claude 命令 & Agent 库

### 命令列表 | Commands (`.claude/commands/`)

| 命令 | 功能 | Function |
|------|------|----------|
| `/research` | 关键词/竞争对手研究，生成 brief | Keyword/competitor research |
| `/write` | 创建完整文章，自动调用 Agent 优化 | Create full article with auto-agent optimization |
| `/rewrite` | 更新已有内容 | Update existing content |
| `/optimize` | SEO 最后优化 | Final SEO polish |
| `/analyze-existing` | 内容健康审计 | Content health audit |
| `/performance-review` | 数据驱动的内容优先级 | Analytics-driven content priorities |
| `/publish-draft` | 发布到 WordPress | Publish to WordPress |
| `/article` | 简化文章创建 | Simplified article creation |
| `/cluster` | 主题集群策略（支柱+支撑+内链） | Topic cluster strategy |
| `/priorities` | 内容优先级矩阵 | Content prioritization matrix |
| `/research-serp` | SERP 搜索结果分析 | SERP analysis |
| `/research-gaps` | 内容差距分析 | Content gap analysis |
| `/research-trending` | 热门趋势研究 | Trending topics research |
| `/research-ai-citations` | AI 引用审计 | AI citation audit |
| `/repurpose` | 适配到 LinkedIn/Medium/Reddit/Quora | Multi-platform content repurposing |
| `/landing-write` / `/landing-audit` / `/landing-research` | 着陆页全流程 | Landing page workflow |
| `/landing-publish` / `/landing-competitor` | 着陆页发布与竞品分析 | Landing page publish & competitor analysis |

### Agent 角色 | Agent Personas (`.claude/agents/`)

| Agent | 角色 | Role |
|-------|------|------|
| `seo-optimizer` | SEO 优化师 | SEO Optimizer |
| `content-analyzer` | 内容分析师 | Content Analyst |
| `meta-creator` | Meta 创作者 | Meta Creator |
| `internal-linker` | 内链策略师 | Internal Linker |
| `keyword-mapper` | 关键词映射师 | Keyword Mapper |
| `editor` | 编辑 | Editor |
| `headline-generator` | 标题生成器 | Headline Generator |
| `cro-analyst` | CRO 分析师 | CRO Analyst |
| `performance` | 绩效分析师 | Performance Analyst |
| `cluster-strategist` | 集群策略师 | Cluster Strategist |
| `landing-page-optimizer` | 着陆页优化师 | Landing Page Optimizer |

---

## 📂 项目结构 | Project Structure

```
seomachine/
├── bin/
│   └── seomachine          # CLI 入口工具
├── data_sources/
│   ├── modules/             # 24 个 Python 分析模块
│   ├── config/              # API 配置 (GA4, GSC, DataForSEO)
│   └── requirements.txt     # Python 依赖
├── .claude/
│   ├── commands/            # 24 个 Claude 命令
│   ├── agents/              # 11 个 Claude Agent 角色
│   └── skills/              # Claude 技能 (CRO, Analytics, SEO Audit 等)
├── context/                 # 品牌/SEO 指南库
├── research_*.py            # 10 个独立研究脚本
├── seo_*.py                 # SEO 分析脚本
├── CLAUDE.md                # Claude Code 工作空间配置
└── bin/seomachine           # Hermes Agent CLI 工具
```

---

## 🔌 数据源集成 | Data Source Integration

| 数据源 | 功能 | 是否需要 API Key |
|--------|------|-----------------|
| **Google Analytics 4** | 流量/互动数据 | ✅ 需要 GA4 服务账号 |
| **Google Search Console** | 搜索排名/展示数据 | ✅ 需要 GSC 服务账号 |
| **DataForSEO** | SERP 数据/关键词指标 | ✅ 需要 DataForSEO 账号 |
| **WordPress** | Yoast SEO 发布 | ✅ 需要 WP REST API 权限 |

配置方式：复制 `data_sources/config/.env.example` → `data_sources/config/.env`，填入你的 API 凭据。

---

## 🗺 后续计划 | Roadmap

- [x] CLI 命令封装 (Hermes Agent 兼容)
- [x] GitHub 托管
- [ ] GA4/GSC/DataForSEO 集成文档
- [ ] 中文关键词的 NLP 增强分析
- [ ] 批量 SEO 报告生成
- [ ] 百度搜索兼容适配

---

## 📄 许可证 | License

[MIT License](LICENSE)

原始项目：[TheCraigHewitt/seomachine](https://github.com/TheCraigHewitt/seomachine) © Craig Hewitt  
Adaptation & CLI wrapper © Sambaba9

---

**如果这个项目对你有帮助，欢迎 Star ⭐ 支持！**  
**If you find this project useful, please consider giving it a Star ⭐!**
