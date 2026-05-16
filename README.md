# Self-Evolution Agent

> Agent 知识自进化实验项目

---

## 项目定位

**目标**: 构建 Agent 知识自进化能力，实现"越用越聪明"

**与 openclaw-workspace 关系**:
- `self-evolution-agent` = 知识仓库（Wiki + Sources）
- `openclaw-workspace` = Agent 大脑（控制 + 记忆）

---

## 目录结构

```
self-evolution-agent/
├── wiki/           # 结构化知识层
│   ├── concepts/   # 概念定义
│   ├── people/     # 人物卡片
│   ├── companies/  # 公司信息
│   ├── topics/     # 主题聚合
│   ├── research/   # 调研报告
│   ├── index.md    # 全局索引
│   ├── hot.md      # 最近快照
│   └── log.md      # 时间线
│
├── sources/        # 原始资料层
│   ├── articles/   # 文章存档
│   ├── papers/     # 论文 PDF
│   ├── videos/     # 视频记录
│   └── sessions/   # 会话备份
│
├── skills/         # Wiki 操作 Skills
│
├── .learnings/     # 学习沉淀
│   ├── LEARNINGS.md
│   ├── ERRORS.md
│   └── FEATURE_REQUESTS.md
│
└── README.md
```

---

## Wiki 操作流程

### Ingest (知识摄入)
```
新资料 → sources/ 存档
       → LLM 提取要点
       → wiki/ 页面
       → index.md 更新
       → wikilink 建立
```

### Query (知识查询)
```
提问 → index.md 定位
     → wiki/ 页面阅读
     → 综合答案 + 引用
```

### Lint (知识维护)
```
定期检查 → 矛盾/过时内容
        → 孤儿页面清理
        → 引用补全
```

---

## 学习循环

```
错误/纠正 → .learnings/
    ↓
heartbeat review
    ↓
promote → AGENTS.md / TOOLS.md
    ↓
指导 Agent 行为
```

---

## 技术参考

- LLM Wiki 三层架构
- Obsidian-Wiki Skills 机制
- GBrain 分层检索策略

---

**创建时间**: 2026-05-16
**Git**: https://github.com/junboyuan/self-evolution-agent