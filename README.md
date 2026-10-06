# DD 完整提交包

版本：5.0.3-recovery-candidate，协议：dd-selfproto-v1.3。

完整提交包见本仓库 Releases 的 **DD 完整提交包 · 2026-10-06**。原 ZIP 共 5,646,534,682 字节，因 GitHub 单个 Release 附件限制，按原始字节拆为三个分卷。请下载全部三个分卷和合并说明，合并后解压。

合并后 ZIP 的 SHA256：
`4f3ed4b5164bfd052d9e699da6b47726450fe1cd0dac3af65896732295ebb096`

提交包含任务实现、Baseline/Reference、模型及真实运行证据。小规模试跑结论与自检 checklist 也随 Release 提供。

双独立质检（gpt-6.1-sol、gpt-6-astra）结论均为 PASS，适用已确认的 dd-user-20261005 验收口径。正式成对评测 n=1，FID-50k 从 9.800032 降至 9.749575，归一化得分 0.327963；不作多 seed 稳定性或 3σ 声明。
