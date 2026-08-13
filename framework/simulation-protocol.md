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

Canonical repository:

`sumrian/fde-training-lab`

完成复盘后，需要形成并同步以下训练资产：

- `simulations/<id>/scenario.md`
- `simulations/<id>/final-proposal.md`
- `simulations/<id>/review.md`
- `simulations/<id>/score.yaml`
- `progress/current-profile.md`
- `progress/score-history.csv`

有可复用原则或跨案例模式时，同时更新：

- `playbook/`
- `progress/recurring-patterns.md`

### GitHub Sync Rule

如果当前环境具备 GitHub 写权限：

1. 复盘完成后直接把以上变更写回 `sumrian/fde-training-lab`；
2. 不要求用户手工复制复盘内容；
3. 写入前基于仓库当前内容进行更新，避免盲目覆盖历史记录；
4. 写入后明确告知哪些文件已更新；
5. 推荐每个完整 Case 使用一个清晰的提交，例如：

   `training: complete simulation <id>`

如果 GitHub 不可用、没有写权限或写入失败：

- 不得声称已经同步成功；
- 明确说明失败点；
- 输出需要新增或修改的确切文件内容，供后续同步。

### Responsibility

ChatGPT Project / Work：

> 负责模拟、讨论、复盘和动态上下文。

GitHub：

> 负责长期 canonical knowledge、case history、scores 和 current profile。

训练闭环为：

> Simulation → Final Proposal → Review → Distill → GitHub Sync → Next Simulation

## Anti-pattern

不要：

- 为了让用户成功而降低业务难度
- 每轮改变评分标准
- 只评价措辞是否礼貌
- 用最后方案质量掩盖 Discovery 过程问题
- 用“总分提升”代替具体弱点训练
- 复盘后只停留在聊天里而不沉淀训练资产（当 GitHub 写权限可用时）
