# PLMediaStreamingKit Release Notes for 3.0.3

## 内容

- [简介](#简介)
- [问题反馈](#问题反馈)
- [记录](#记录)

## 简介

PLMediaStreamingKit 为 iOS 开发者提供直播推流 SDK。

## 问题反馈

当你遇到任何问题时，可以通过在 GitHub 的 repo 提交 ```issues``` 来反馈问题，请尽可能的描述清楚遇到的问题，如果有错误信息也一同附带，并且在 ```Labels``` 中指明类型为 bug 或者其他。

[通过这里查看已有的 issues 和提交 Bug](https://github.com/pili-engineering/PLMediaStreamingKit/issues)

## 记录

- 功能
   - 支持获取麦克风数据 asbd 信息
   - 支持重新加载音频推流编码配置信息
   - 流信息回调新增音视频码率信息

- 缺陷    
   - 修复摄像头未授权情况下设置动态码率 crash 的问题
   - 修复快速多次 start 后立即 stop 视频仍在发布的问题
   - 解决 reloadConfiguration 更改编码帧率无效的问题
   - 解决连接蓝牙耳机后采集实际输入源是设备麦克风的问题
   - 修复音频采集配置 44100 长时间推流拉流端音画不同步的问题
   - 修复使用带声音的三方键盘及蓝牙耳机同时连接电脑手机 message 线程偶现 crash 的问题

## 注意事项

- **从 v3.0.1 开始，HappyDNS 版本更新至 v0.3.17**
- **从 v3.0.0 版本开始，七牛直播推流 SDK 需要先获取授权才能使用。授权分为试用版和正式版，可通过 400-808-9176 转 2 号线联系七牛商务咨询，或者 [通过工单](https://support.qiniu.com/?ref=developer.qiniu.com) 联系七牛的技术支持。**
- **v3.0.0 之前的版本不受影响，请继续放心使用。**
- **老客户升级 v3.0.0 版本之前，请先联系七牛获取相应授权，以免发生鉴权不通过的现象。**
- 基于 114 dns 解析的不确定性，使用该解析可能会导致解析的网络 ip 无法做到最大的优化策略，进而出现推流质量不佳的现象。因此建议使用非 114 dns 解析
