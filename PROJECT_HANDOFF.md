# Academic Research Agents — 项目交接文档

> 最后更新：2026-03-23
> 项目地址：https://github.com/zyx312/academic-research-agents
> 作者：张玉新，吉林大学汽车工程学院教授

---

## 一、项目定位

面向高校科研全流程的 Claude Code Agent 开源项目，灵感来自 automotive-claude-code-agents（博世工程师 Thejeswarareddy R 的项目）。用同样的架构模式（Skills + Agents + Commands + Hooks + Workflows），覆盖学术研究的完整生命周期。

**目标用户：** 高校教授、博士/硕士研究生、科研团队

**商业潜力：** 开源引流 → 付费知识库 → SaaS团队版（实验室管理）

---

## 二、当前状态

### 已完成

| 组件 | 数量 | 行数 | 状态 |
|------|------|------|------|
| **Skills（技能文件）** | 44个，11个类别 | 18,969行 | ✅ 全部填充了深度内容 |
| **Agents（智能体）** | 11个 | ~200行 | ⚠️ 仍为模板，需写系统Prompt |
| **Workflows（工作流）** | 5个 | ~100行 | ⚠️ 仍为模板，需深化 |
| **Commands（命令）** | 目录已建 | — | ❌ 未开始 |
| **Hooks（钩子）** | 目录已建 | — | ❌ 未开始 |
| **Knowledge（知识库）** | 目录已建 | — | ❌ 未开始 |
| **install.sh** | 1个 | 可用 | ✅ 追加式安装，academic-前缀 |
| **README.md** | 1个 | 可用 | ⚠️ 需更新以反映新内容规模 |

### 已删除

- `skills/proposal/nsfc.md` — NSFC太区域化、项目类型太多，已移除

### Skill文件11个类别详情

| 类别 | 文件数 | 行数 | 内容来源 |
|------|--------|------|---------|
| literature/ | 4 | ~1,700 | PRISMA, Keshav三遍法, Zotero高级配置, 12个数据库检索语法 |
| paper-writing/ | 6 | ~2,700 | Simon Peyton Jones, Stanford Widom, gpt_academic Prompt, CALM rebuttal |
| peer-review/ | 2 | ~700 | 结构化评审模板, 编辑沟通策略 |
| patent/ | 4 | ~1,550 | 五种挖掘法, CNIPA完整时间线, 权利要求书 |
| proposal/ | 4 | ~1,550 | 通用8组件框架, 横向课题合同, ACE答辩法 |
| student-mentoring/ | 5 | ~2,300 | IDP, 本科28周/硕士2-3年/博士4-5年时间线, PhD生存指南 |
| project-execution/ | 4 | ~1,700 | 风险矩阵, 预算合规, 审计自查清单 |
| data-management/ | 4 | ~1,950 | FAIR原则, Datasheets框架, 8种许可证, GDPR/中国数安法 |
| teaching/ | 4 | ~1,300 | Backward Design, Bloom分类, SoTL框架 |
| academic-impact/ | 4 | ~1,150 | LinkedIn算法, 标题公式, 跨平台策略 |
| career/ | 3 | ~1,000 | 人才计划申报, H-index追踪, 学术CV 13段结构 |

### 融入的GitHub开源项目精华

| 项目 | Stars | 融入内容 |
|------|-------|---------|
| gpt_academic | 70,291 | 论文润色/翻译/语法纠错Prompt |
| ChatGPT-Academic-Prompt | 760 | 顶会/Nature风格改写Prompt |
| AI-research-tools | 3,060 | ESODA/Linggle/ccfddl等工具 |
| awesome-scientific-writing | 922 | Vale/LanguageTool等lint工具 |
| awesome-phd-advice | 2,043 | 经典PhD生存指南集合 |
| awesome-research-proposals-guide | 200 | 8组件提案框架 |
| awesome-research | 2,548 | Zenodo/ORCID/Figshare等工具 |

---

## 三、待完成事项（按优先级排序）

### P0 — 现有Skill质量提升（用户明确提出"还不够深度和实用"）

每个skill文件需要：
1. **更多真实案例** — 不只是框架和模板，要有具体的好/坏示例对比
2. **更细化的Prompt** — 当前Prompt偏通用，需要针对具体场景细化
3. **工具集成代码** — 部分skill提到了工具但没有给出实际配置/代码
4. **中英双语** — 当前大部分内容是英文，国内用户需要中文版本

**建议方法：** 针对每个类别，在GitHub上搜索更多同类项目（上轮已搜索一批，可继续深挖），提取具体的模板、配置文件、脚本等可直接使用的素材。

### P1 — Agent系统Prompt（11个文件）

当前11个Agent文件都是模板，需要写真正的系统Prompt：

```
agents/
├── literature-researcher.md      # 文献研究员
├── paper-coauthor.md              # 论文协作者
├── peer-reviewer.md               # 审稿助手
├── patent-strategist.md           # 专利策略师
├── proposal-advisor.md            # 基金申请顾问
├── thesis-supervisor.md           # 论文指导助手
├── data-steward.md                # 数据管理员
├── project-manager.md             # 科研项目经理
├── academic-writer.md             # 学术写作教练
├── teaching-assistant.md          # 教学助手
└── impact-strategist.md           # 影响力策略师
```

每个Agent需要：
- 角色定义和专业背景
- 可调用的Skill列表
- 交互模式（问答、引导、审查）
- 输出格式规范

### P2 — Workflow端到端深化（5个文件）

```
workflows/
├── undergrad-thesis-flow.md       # 本科毕设全流程
├── paper-publication-flow.md      # 论文发表全流程
├── patent-flow.md                 # 专利全流程
├── nsfc-flow.md                   # 需要重命名或删除（已删nsfc skill）
└── phd-journey-flow.md            # 博士全程
```

注意：`nsfc-flow.md` 需要改为通用的 `grant-proposal-flow.md`

### P3 — Commands / Hooks / Knowledge

- Commands：快捷命令（如 `/lit-search`, `/paper-outline`）
- Hooks：自动化检查（提交前查重、引用格式检查）
- Knowledge：知识库文档（期刊投稿指南、学位要求等）

### P4 — README更新 + 推广

- 更新README反映当前18,969行的规模
- 写一篇公众号推广文章（复用AutoSafeAgent的成功路径）
- 写一篇LinkedIn post
- 在相关GitHub项目下做cross-reference

---

## 四、项目架构说明

```
academic-research-agents/
├── install.sh          # 追加式安装，academic-前缀，不改现有环境
├── uninstall.sh        # 一键卸载
├── README.md           # 项目说明
├── LICENSE             # MIT, 2026, Yuxin Zhang
├── CONTRIBUTING.md     # 贡献指南
├── PROJECT_HANDOFF.md  # 本文档
│
├── skills/             # 44个技能文件，11个类别
├── agents/             # 11个智能体（待深化）
├── commands/           # 快捷命令（待建设）
├── hooks/              # 自动化钩子（待建设）
├── knowledge/          # 知识库（待建设）
└── workflows/          # 5个端到端工作流（待深化）
```

安装方式与 automotive-claude-code-agents 完全一致：
```bash
git clone https://github.com/zyx312/academic-research-agents.git
cd academic-research-agents
./install.sh                    # 安装
./install.sh --uninstall        # 卸载
```

---

## 五、与其他项目的关系

| 项目 | 关系 |
|------|------|
| automotive-claude-code-agents (Fork) | 灵感来源，架构模式完全复用 |
| AutoSafeAgent公众号文章 | 推广路径的成功验证（3000+阅读，数百关注） |
| 驭研科技 | 潜在的商业化载体（SaaS版） |
| 吉大教学 | 第一批用户（学生试用并反馈） |

---

## 六、重启项目时的建议步骤

1. 读取本文档，了解当前状态
2. `cd /Users/zyx/Desktop/WorkToDo/academic-research-agents && git pull`
3. 选择一个P0类别的skill文件，深入改进
4. 改进方法：在GitHub上搜索该类别的顶级开源项目，提取真实案例和可执行素材
5. 每完善3-5个文件后提交推送
6. 当P0完成后，转向P1（Agent系统Prompt）

---

*本文档由 Claude Code 生成，供后续会话读取使用。*
