# 任务族映射

## 目标

Map work into a small set of families so `OS-原力` can adapt artifact names without changing the underlying method.

## Mode Selection

### `full mode`

Use when any of these are true:

- the task is multi-stage
- multiple skills or tools are likely
- the task affects money, trust, launch, or external communication
- the user explicitly asks for deep thinking or a full walkthrough

### `light mode`

Use when all of these are true:

- the task is short
- the task is low-risk
- the execution path is obvious
- a compressed visible output is sufficient

`light mode` may shorten the visible artifact pack, but must not skip the three gates.

## Families

### 1. 内容生产

#### Trigger Signals

- 写文章
- 公众号
- 标题
- 大纲
- 内容策划
- 视频脚本

#### Artifact Pack

- `Theme Brief`
- `Strategy Card`
- `Execution Run Sheet`
- `Publish Pack`
- `Evolution Note`

#### Theme Gate

Ask:

- 这个内容主题值不值得进入当前主战场？
- 它服务品牌、销售、认知资产，还是只是一次性热点？

#### Strategy Gate

State:

- target reader
- core promise
- current strategy layer
- evidence needs
- risk boundaries

#### Default Stop Conditions

- no clear reader
- no real objective
- only topical heat with no compounding value
- structure not confirmed but draft requested

### 2. 研究审计

#### Trigger Signals

- 审计
- 盘点
- 研究
- benchmark
- review
- compare

#### Artifact Pack

- `Inquiry Brief`
- `Analysis Card`
- `Audit Run Sheet`
- `Audit Pack`
- `Evolution Note`

#### Theme Gate

Ask:

- 这轮研究是否服务一个真实决策？
- 范围是否收敛到可验证的问题？

#### Strategy Gate

State:

- current evidence surface
- current strategy layer
- comparison lens
- proof standard

#### Default Stop Conditions

- the research question is still vague
- the evidence surface is too weak for the claim
- the output would be a summary without decision value

### 3. 工作流自动化

#### Trigger Signals

- workflow
- automation
- n8n
- Dify
- Coze
- 飞书工作流

#### Artifact Pack

- `Automation Brief`
- `Design Card`
- `Build Run Sheet`
- `Delivery Pack`
- `Evolution Note`

#### Theme Gate

Ask:

- 这个自动化是否真的值得做，而不是一次性 annoyance？
- 自动化目标是否清楚到可以 design 和 verify？

#### Strategy Gate

State:

- orchestration target
- system choice rationale
- current strategy layer
- verification path

#### Default Stop Conditions

- source and destination are unclear
- no clear trigger / input / output contract
- verification path is missing

### 4. 接线部署

#### Trigger Signals

- deploy
- 上线
- 接 webhook
- 绑定平台
- connect
- release

#### Artifact Pack

- `Rollout Brief`
- `Rollout Card`
- `Deployment Run Sheet`
- `Release Pack`
- `Evolution Note`

#### Theme Gate

Ask:

- 现在是不是正确的 rollout timing？
- 这是试验性验证还是正式外部 release？

#### Strategy Gate

State:

- rollout objective
- risk class
- current strategy layer
- rollback and verification plan

#### Default Stop Conditions

- external side effects are irreversible but not approved
- rollback path is unclear
- success criteria are missing

### 5. 治理协作

#### Trigger Signals

- 组织设计
- 治理
- 协同
- 路由
- capability mapping
- roadmap

#### Artifact Pack

- `Governance Brief`
- `Policy Card`
- `Governance Run Sheet`
- `Decision Pack`
- `Evolution Note`

#### Theme Gate

Ask:

- 这是否真的是治理问题，而不是领域执行问题？
- 这轮治理是否会减少未来摩擦？

#### Strategy Gate

State:

- current system distortion
- desired operating rule
- current strategy layer
- adoption path

#### Default Stop Conditions

- the issue is one-off, not structural
- the proposal creates more protocol weight than it removes

### 6. 未知或混合任务

#### Trigger Signals

- request spans multiple families
- request is still too blurry after compression
- no single family clearly dominates

#### Artifact Pack

- `Task Brief`
- `Strategy Card`
- `Execution Run Sheet`
- `Result Pack`
- `Evolution Note`

#### Default Stop Conditions

- no dominant objective
- no smallest viable family
- decomposition is still unstable

## Routing Note

Only the content family has a fixed canonical chain in this v1.

All other families should default to `skill-router`, then choose the smallest valid domain chain.

## 高阶混合模式：系统行为审计

Some requests are bigger than one family.

If the user asks for:

- 系统盘点
- skill 生态审计
- 行为审计
- maturity review
- scorecard
- 历史 run / artifacts 审计

classify the work as:

`研究审计 + 治理协作`

and force:

- `full mode`
- explicit scoring
- explicit deduction reasons
- explicit improvement roadmap

### Default Audit Output

Use the research-audit pack as the primary visible surface:

- `Inquiry Brief`
- `Analysis Card`
- `Audit Run Sheet`
- `Audit Pack`
- `Evolution Note`

Then append a governance annex when the work leads to operating-rule conclusions:

- `Decision Pack`

### Required Audit Extras

For system-wide audits, always add:

- `System Scorecard`
- `Subsystem Scorecards`
- `Deduction Ledger`
- `Roadmap`

If the user wants the audit to become a long-lived operating surface, also add:

- `External Intel`
- `Benchmark Links`
- `Recursion Queue`

Keep local audit artifacts canonical. Treat Feishu as the collaboration surface, not the truth source.

Use [audit-rubric.md](audit-rubric.md) as the only scoring model.

Use [system-audit-playbook.md](system-audit-playbook.md) as the execution recipe.

### Default Stop Conditions

Stop or narrow the audit if:

- the evidence surface is too weak
- the time boundary is undefined
- the object being audited is not clearly named
- the output would become a giant inventory dump rather than a decision-grade scorecard
