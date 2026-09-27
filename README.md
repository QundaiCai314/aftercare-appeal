# aftercare-appeal 1.0.0

售后助手第十个 Skill：根据已核实的售后结果、平台复核要求、真实凭证及处理记录，判断是否适合平台内复核并准备可由用户核对的申诉草稿。

不提交申诉、不操作网页、不联系商家或客服，不处理平台外投诉、仲裁、诉讼或法律结论。公开包只包含合成材料和开发文档，不含真实订单、凭证或个人信息。

## 下载与资料

- [可加载 Skill 包](aftercare-appeal-1.0.0.zip)：解压后使用 `aftercare-appeal/`。
- [完整工程交付](aftercare-appeal-1.0.0-full.zip)：包含 Skill、测试、合成场景、结构校验、接口摘录及提案。
- [测试报告](测试报告.md)
- [契约修订提案](契约修订提案.md)
- [文件 SHA-256](SHA256SUMS.json)

中央契约保持 1.0.0，未改中央 Schema 或 catalog。项目 catalog 仍为 `design_not_implementation`，Skills 未实现状态不因本包改变。申诉草稿完成不代表用户已核对、允许发送或申诉成功。

## 验证与限制

26 个本地确定性检查通过，合成请求/结果通过包内 Schema 子集校验。当前环境缺少 PyYAML，因此 Skill Creator 快速校验未能执行；未安装任何依赖。没有独立模型前向测试、真实平台联调或申诉提交。

宿主仍需实现引用真实性/任务范围、草稿版本化核对、内容和文件绑定授权、未知发送阻断、申诉实例及台账去重。接口缺口和最小迁移提案单独列出，未作为已生效契约。

仅加载 Skill 包不需运行脚本。完整包本地检查命令：`python -B -m unittest discover -s tests -v`；请求/结果样例结构检查：`python scripts/validate_samples.py`（从 Skill 包目录运行）。
