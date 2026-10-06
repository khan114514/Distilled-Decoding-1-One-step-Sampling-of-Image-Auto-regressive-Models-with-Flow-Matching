# DD 完整提交包

版本：5.0.3-recovery-candidate，协议：dd-selfproto-v1.3。

完整提交包由原 ZIP 按字节拆为三个分卷，通过 Git LFS 存放在 [submission](submission/) 目录。下载以下全部三个分卷，合并后解压：

- [分卷 001](https://media.githubusercontent.com/media/khan114514/Distilled-Decoding-1-One-step-Sampling-of-Image-Auto-regressive-Models-with-Flow-Matching/main/submission/DD_complete.zip.001)
- [分卷 002](https://media.githubusercontent.com/media/khan114514/Distilled-Decoding-1-One-step-Sampling-of-Image-Auto-regressive-Models-with-Flow-Matching/main/submission/DD_complete.zip.002)
- [分卷 003](https://media.githubusercontent.com/media/khan114514/Distilled-Decoding-1-One-step-Sampling-of-Image-Auto-regressive-Models-with-Flow-Matching/main/submission/DD_complete.zip.003)

若使用 Git 克隆，请先安装 Git LFS；仓库自动生成的源码 ZIP 可能仅包含 LFS 指针，请使用上面的分卷下载链接。

macOS / Linux：
```sh
cat DD_complete.zip.001 DD_complete.zip.002 DD_complete.zip.003 > DD_complete.zip
shasum -a 256 DD_complete.zip
```
Windows 命令提示符：
```bat
copy /b DD_complete.zip.001+DD_complete.zip.002+DD_complete.zip.003 DD_complete.zip
certutil -hashfile DD_complete.zip SHA256
```

合并后文件大小：5,646,534,682 字节。合并后 SHA256：
`4f3ed4b5164bfd052d9e699da6b47726450fe1cd0dac3af65896732295ebb096`

各分卷校验值见 [SHA256SUMS.txt](SHA256SUMS.txt)，详细步骤见 [合并说明](合并说明.txt)。

提交包含任务实现、Baseline/Reference、模型及真实运行证据。另附 [小规模试跑结论](小规模试跑结论.txt) 和 [自检 checklist](自检checklist.txt)。

双独立质检（gpt-6.1-sol、gpt-6-astra）结论均为 PASS，适用已确认的 dd-user-20261005 验收口径。正式成对评测 n=1，FID-50k 从 9.800032 降至 9.749575，归一化得分 0.327963；不作多 seed 稳定性或 3σ 声明。
