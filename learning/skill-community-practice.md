# Skill 社区实践与思想哲学

> 来源：GitHub awesome-agent-skills (549+ skills) + Anthropics 官方 + 知识库宪法式设计
> 更新：2026-03-20

---

## 一、社区生态概览

### 1.1 Skill 定义

Skill（技能）是一种让 AI Agent 具备特定领域能力的扩展机制。通过 `SKILL.md` 定义：
- **触发条件**：什么场景下调用
- **执行逻辑**：如何完成任务
- **边界约束**：什么不能做

### 1.2 生态规模

| 指标 | 数量 |
|------|------|
| GitHub topic 下的仓库 | 1,324+ |
| awesome-agent-skills 收录 | 549+ |
| 官方 Anthropic skills | 16+ |
| 大厂官方 skills | 50+ (Vercel, Stripe, Cloudflare, Expo, etc.) |

---

## 二、官方 Anthropic Skills 分类

### 2.1 文档处理

| Skill | 用途 |
|-------|------|
| docx | 创建、编辑、分析 Word 文档 |
| pptx | 创建、编辑、分析 PowerPoint |
| xlsx | 创建、编辑、分析 Excel 表格 |
| pdf | 提取文本、创建 PDF、处理表单 |

### 2.2 前端与设计

| Skill | 用途 |
|-------|------|
| frontend-design | 前端设计与 UI/UX 开发 |
| web-artifacts-builder | 构建复杂 React+Tailwind HTML |
| canvas-design | PNG/PDF 格式视觉艺术设计 |
| algorithmic-art | p5.js 生成艺术（随机种子） |
| theme-factory | 用主题样式化 artifacts |
| slack-gif-creator | 创建 Slack 优化的 GIF |

### 2.3 工具与集成

| Skill | 用途 |
|-------|------|
| mcp-builder | 创建 MCP 服务器集成外部 API |
| webapp-testing | 用 Playwright 测试本地 Web 应用 |
| brand-guidelines | 应用 Anthropic 品牌色彩和字体 |

### 2.4 内部协作

| Skill | 用途 |
|-------|------|
| internal-comms | 写状态报告、新闻稿、FAQ |
| doc-coauthoring | 协作文档编辑与共创 |

### 2.5 元技能

| Skill | 用途 |
|-------|------|
| skill-creator | 创建扩展 Claude 能力的技能 |
| template | 创建新技能的基础模板 |

---

## 三、大厂官方 Skills

### 3.1 Vercel

- **next-best-practices** — Next.js 最佳实践和推荐模式
- **next-cache-components** — 缓存策略和缓存感知组件
- **next-upgrade** — 升级 Next.js 项目
- **react-best-practices** — React 最佳实践
- **composition-patterns** — React 组件组合模式
- **vercel-deploy** — 部署项目到 Vercel
- **web-design-guidelines** — Web 设计标准

### 3.2 Stripe

- **stripe-best-practices** — Stripe 集成最佳实践
- **upgrade-stripe** — 升级 Stripe SDK 和 API 版本

### 3.3 Cloudflare

- **cloudflare** — Workers, Pages, 存储, AI, 网络
- **agents-sdk** — 构建有状态的 AI agents
- **building-ai-agent-on-cloudflare** — 有状态 agent 和 WebSockets
- **building-mcp-server-on-cloudflare** — 构建 MCP 服务器
- **durable-objects** — 有状态协调（RPC, SQLite, WebSockets）
- **wrangler** — 部署和管理 Workers, KV, R2, D1 等
- **web-perf** — 审计 Core Web Vitals

### 3.4 Expo

- **expo-app-design** — 设计和构建 Expo 应用
- **expo-deployment** — 部署 Expo 应用到生产
- **upgrading-expo** — 升级 Expo SDK 版本

### 3.5 Supabase

- **postgres-best-practices** — Supabase PostgreSQL 最佳实践

### 3.6 其他大厂

| 厂商 | Skills |
|------|--------|
| HashiCorp | terraform-code-generation, terraform-module-generation, terraform-provider-development |
| Sanity | sanity-best-practices, content-modeling-best-practices, seo-aeo-best-practices |
| ClickHouse | ClickHouse 最佳实践 |
| Netlify | netlify-functions, netlify-edge-functions, netlify-blobs, netlify-db |
| Google Labs (Stitch) | design-md, enhance-prompt, react-components, shadcn-ui |
| Better Auth | best-practices, commands, create-auth |
| Hugging Face | (官方 skill 列表) |
| Trail of Bits | (安全相关 skills) |

---

## 四、社区思想哲学

### 4.1 核心理念

1. **能力块（Capability Block）** — Skill 是可组合的能力单元
2. **即插即用** — 通过描述触发，无需修改核心系统
3. **渐进式披露** — 入口简洁，细节按需加载
4. **社区验证** — 真实工程团队创建和维护，非批量 AI 生成

### 4.2 与知识库"宪法式设计"的呼应

| 知识库原则 | 社区实践 |
|-----------|----------|
| 约束 > 步骤 | Skill 只定义边界，不做死板 SOP |
| 二区架构 | docx/pdf 有确定性输出，frontend-design 则灵活 |
| 渐进式披露 | 官方 skill 都是短入口 + 子文件 |
| 自我纠错 | 社区 skill 普遍缺少，需加强 |

---

## 五、安全警告 ⚠️

> **Skills can include prompt injections, tool poisoning, hidden malware payloads, or unsafe data handling patterns.**

### 5.1 三大风险

1. **Prompt 注入** — Skill 描述可能被恶意利用
2. **工具投毒** — Skill 绑定的脚本可能藏恶意代码
3. **数据不安全** — Skill 可能不当处理敏感数据

### 5.2 审计工具

- [Snyk Skill Security Scanner](https://github.com/snyk/agent-scan)
- [Agent Trust Hub](https://ai.gendigital.com/agent-trust-hub)

### 5.3 使用建议

1. **安装前审查** — 不要盲目安装，看源码
2. **来源验证** — 优先用官方/大厂 skill
3. **最小权限** — 只给必要的工具权限
4. **定期更新** — skill 可能会被恶意修改

---

## 六、创建 Skill 的最佳实践

### 6.1 结构规范

```
skill-name/
├── SKILL.md (必须)
│   ├── YAML frontmatter (name, description 必须)
│   └── Markdown 指令
└── 资源文件 (可选)
    ├── scripts/    # 可执行脚本
    ├── references/ # 参考文档
    └── assets/     # 静态资源
```

### 6.2 Description 写法

- **要具体** — 覆盖触发场景和边缘情况
- **要"pushy"** — 主动引导而非被动等待
- **包含触发词** — 用户可能说的短语

```yaml
# ❌ 不好
name: pdf
description: 处理 PDF 文件

# ✅ 好
name: pdf
description: |
  提取 PDF 文本、创建 PDF、处理表单。
  当用户说"读取 PDF"、"提取 PDF 内容"、"填充 PDF 表单"时触发。
```

### 6.3 渐进式披露

| 层级 | 内容 | 大小 |
|------|------|------|
| 元数据 | name + description | ~100 words |
| 入口 | SKILL.md body | < 500 lines |
| 详细 | 子文件 | 按需加载 |

### 6.4 测试驱动

1. **写 2-3 个真实 test case**
2. **with-skill vs baseline 对比**
3. **量化评估** (pass_rate, time, tokens)
4. **定性反馈** (用户主观评价)

---

## 七、Skill vs MCP vs Prompt

| 维度 | Skill | MCP | System Prompt |
|------|-------|-----|---------------|
| 定位 | 能力扩展 | 工具连接 | 行为定义 |
| 触发 | description 匹配 | 按需调用 | 始终生效 |
| 复杂度 | 低-中 | 中-高 | 低 |
| 维护 | 用户自己 | 开发者 | 系统级 |

---

## 八、参考资料

- [awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) — 549+ skills 收录
- [anthropics/skills](https://github.com/anthropics/skills) — 官方 skills
- [Model Context Protocol](https://modelcontextprotocol.io) — MCP 协议
- [Anthropic Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) — 官方 Agent 最佳实践

---

## 九、一句话总结

> **Skill = 社区验证的能力块 + 宪法式设计约束 + 安全审计意识**
