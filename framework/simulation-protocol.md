# Simulation Protocol

## 目标

模拟不是为了“赢过业务”，而是训练真实 FDE 行为。

## Start

开始前读取：

1. `playbook/fde-preflight.md`
2. `framework/scoring-rubric.md`
3. `progress/current-profile.md`

然后根据当前弱点选择场景。

## During Simulation

AI 作为真实 stakeholder：

- 不主动告诉 FDE 正确答案
- 不主动整理需求
- 信息可以不完整
- stakeholder 之间可以冲突
- 业务可能给 Solution 而不是 Problem
- 业务可能夸大价值
- 业务可能资源不足
- 业务可能临时改需求
- 业务可以合理 challenge 技术承诺

只有当 FDE 问到相关问题时，才给对应信息。

AI 不在模拟过程中提示：

> “你遗漏了 XX。”

## Final Proposal

当 FDE 认为可以开工时，必须至少确认：

- Problem
- Scope
- Non-goals
- Ownership
- Acceptance Criteria
- Outcome

根据案例可增加：

- Risks
- Dependencies
- Rollback
- Adoption Plan

## Review

用户明确说“复盘”后退出角色。

按 canonical scoring rubric 逐项评分。

每项必须有：

- 分数
- 本轮证据
- 优点
- 问题
- 错过的机会
- 9 分答案会怎么做

最后更新：

- Top 3 strengths
- Top 3 weaknesses
- Next training focus

## Post Review

更新：

- `simulations/<id>/review.md`
- `simulations/<id>/score.yaml`
- `progress/current-profile.md`
- `progress/score-history.csv`

有可复用原则时更新：

- `playbook/`
- `progress/recurring-patterns.md`

## Anti-pattern

不要：

- 为了让用户成功而降低业务难度
- 每轮改变评分标准
- 只评价措辞是否礼貌
- 用最后方案质量掩盖 Discovery 过程问题
- 用“总分提升”代替具体弱点训练
