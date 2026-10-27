# 地点层｜REGION00 蓝灯装配审计 v0.2

## 基线

- 前一地点层 HEAD：b510060503b4a5b60cdf1737efcf7981bddac73d
- 本轮目标：仅调整 REGION00 的灯色与装配语义。

## 一、REGION00 装配

`worldbook/locations/regions/REGION00_栖江市总体概念与区域骨架.md`

现行定义：

- 灯色：蓝灯；
- enabled：true；
- constant：true；
- keywords：[]；
- 职责：提供栖江市主舞台稳定城市底板。

原因：REGION00 定义的是主舞台的城市尺度、地理骨架、六区关系、交通结构与异模办覆盖方式。这些信息属于所有栖江场景都需要共享的基础上下文，不应依赖“栖江市”等关键词命中后才出现。

结果：PASS。

## 二、绿灯边界

以下条目保持关键词触发，不改为常驻：

- REGION01～REGION06：六大具体区域；
- EXT01～EXT06：六座外部城市。

因此 REGION00 常驻不会导致六区详细文本与外部城市同时注入上下文。

结果：PASS。

## 三、设定层隔离

- BLUE01～BLUE10：未修改；
- GREEN01～GREEN46：未修改；
- REGION00 属于“地点层蓝灯”，不是新增一条设定层 BLUE11；
- 地点层与设定层继续使用各自 manifest 管理，不改变已封版设定层编号与职责。

结果：PASS。

## 四、manifest

新增：

`manifest/worldbook-locations.v0.2.json`

装配策略由单一 `keyword_triggered` 升级为 `mixed_blue_green`：

- `blue_entries`：仅 REGION00；
- `green_regions`：REGION01～REGION06；
- `external_cities`：EXT01～EXT06；
- `sites`：仍为空，等待后续核心地点生产。

旧 `worldbook-locations.v0.1.json` 作为历史版本保留，不参与后续正式装配。

# 审计结论

**REGION00_BLUE_ALWAYS_ON_QA_PASS**
