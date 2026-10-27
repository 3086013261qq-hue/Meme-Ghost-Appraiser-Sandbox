# 梗小鬼鉴赏官 / Meme Ghost Appraiser

基于「咩咩制卡·全栈 v1.0.0」组织的原创开放世界都市灵异角色卡工程。

## 分支策略

- `main`：唯一正式基线分支。
- 不设长期业务分支；世界书、人物、地点、MVU、构建与 QA 通过目录分层与原子提交管理。

## 全栈分层

- `docs/`：设计规范、施工单、冻结说明
- `manifest/`：条目顺序、触发、冻结与构建索引
- `worldbook/settings/`：世界观与核心规则
- `worldbook/characters/`：固定角色、随机 NPC/怪谈生成规则
- `worldbook/locations/`：城市分区与地点条目
- `worldbook/true-hauntings/`：固定真祟隐藏主线
- `mvu/`：每日梗小鬼抽取、状态与 UI
- `runtime/`：运行时桥接与状态逻辑
- `media/`：封面、图标、UI 素材与媒体清单
- `build/`：Candidate JSON/PNG 与构建脚本
- `qa/`：结构、状态、MVU、打包与实机 QA
- `source/original/`：只读原始工具包或母版（后续接入）

## 当前阶段

仅建立仓库骨架；正式世界观、地点、角色与 MVU 内容尚未写入。
