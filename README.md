# Scene English Materials

Scene English 的轻量材料库。应用按需从 GitHub Raw 拉取这里的 JSON 文件，服务器不保存大批内容，只保存用户对 `materialId` / `unitId` 的学习进度。

当前版本 `2026.06.28-003` 包含 9 个材料包、104 个学习单元，覆盖生活、旅游、工作、商业/购物、校园、家庭和职业发展等核心场景。

## 内容原则

- 中文学习说明优先；英文只作为学习目标内容。
- 每个文件保持小颗粒，便于按需加载。
- 不存音频、视频或大文件。
- 外部开放素材只记录来源与许可；具体课程例句优先做人工改写和场景化整理。
- 需要可追溯：每个 pack 保留 `sources`。

## 来源策略

- Tatoeba: 句子下载页标明文件为 CC BY 2.0 FR，部分句子为 CC0；仅小量引用/改写并标注。
- Open English WordNet: 项目说明标明 CC-BY 4.0；适合词汇关系、同义/词族启发。
- Princeton WordNet: 官方许可允许按许可使用、复制、修改、分发；用于词义/词族参考时保留引用。
- Wiktionary: 词条文本为 CC-BY-SA/GFDL；目前只作为人工核对参考，不直接搬运长文本。

## 目录

- `manifest.json`: App 入口索引。
- `materials/scenarios/*.json`: 场景训练包。
- `materials/vocabulary/*.json`: 单词训练包。
- `sources/open-sources.md`: 开放素材来源和授权记录。

## 推荐元数据

`manifest.json` 和每个材料包都维护轻量结构化元数据，供 App 做弱项推荐和覆盖分析：

- `domains`: 内容场景域，例如 `life`、`travel`、`work`、`commerce`。
- `skills`: 训练能力，例如 `speaking`、`spelling`、`problem-reporting`、`meaning-recall`。
- `tags`: 中文/英文主题标签，例如 `退款`、`会议`、`词义`。

单元级材料也可以带 `skills` 和 `tags`，用于后续更细颗粒的推荐。不要在这里存音频、视频或大文件。
