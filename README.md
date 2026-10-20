<p align="center">
  <img src="./hero.webp" alt="千恋＊万花 主视觉" width="100%">
</p>

<p align="center">
  <strong> 热爱操作系统开发 </strong><br>
  C/C++ · Python · Linux 系统编程 · 网络编程 · 嵌入式与安全
</p>

<p align="center">
  <img src="https://img.shields.io/badge/C%2FC%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C/C++">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux">
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git">
</p>

> 把每一个进程、线程和 Socket 都当成需要认真对待的队友。
>
> 主线任务：让系统稳定运行，让异常留下线索，让版本顺利交付。

<p align="center">
  <img src="./characters.webp" alt="柚子社角色横幅" width="900">
</p>

## 技能树

| 分支 | 技能点 |
| --- | --- |
| 编程语言 | C/C++、Python；数据结构、模块化设计、Makefile/CMake、Git |
| Linux 系统编程 | fork/exec、waitpid、daemon、信号、文件 I/O、pread、pipe/dup2、pthread、互斥锁、条件变量、进程间通信 |
| 网络编程 | IPv4/UDP/组播、Socket、bind/sendto/recvfrom、setsockopt、网络字节序、自定义变长协议、多线程流媒体、令牌桶限流 |
| 嵌入式与安全 | ARMv8/飞腾派、TGAM 串口协议、RPMsg/OpenAMP、ROS、TrustZone/OP-TEE CA/TA、TEEC Client API |
| AI 桌面开发 | Python、ThreadingHTTPServer、SQLite、OpenClaw、PyWebView/WebView2、Playwright、Node.js、pytest、Portable 打包 |

## 任务档案

| 任务 | 身份 | 技术关键词 | 关键结果 |
| --- | --- | --- | --- |
| AI 超级员工 Windows 桌面智能工作台 | 软件开发实习生 | Python、SQLite、OpenClaw、WebView2、Playwright、Node.js | 18 次提交，支撑 6+ 版本迭代 |
| 飞腾派脑机接口情绪识别与安全监测系统 | 核心开发 | C/Python、TGAM、共享内存、PyTorch、CNN-BiGRU-Attention、OP-TEE | 核心缓存降低约 93%，模型平均准确率 70.2% |
| IPv4 组播多频道音频流媒体系统 | 核心开发 | UDP 组播、pthread、令牌桶、pread、pipe/dup2 | 支持 100 个逻辑频道，重复流量约减少 90% |

### 01 · AI 超级员工 Windows 桌面智能工作台

`2026.07 - 2026.09` · 软件开发实习生

- 整合 AI 多轮会话、定时任务、媒体生成与发布，以及微信、企微、飞书渠道，形成从素材生成到任务执行的桌面工作流。
- 修复 4 类 OpenClaw/微信启动与切换问题，处理 Provider 清洗、插件自愈与账号回收，补齐 8 组恢复测试，覆盖 2200+ 行。
- 使用 Windows Job 实现 `process_guard`，统一看护 Worker、OpenClaw 网关、扫码登录 CLI 与自动化脚本，并在安装、卸载时清理残留进程。
- 参与 18 次代码提交，支撑 6+ 版本迭代，维护版本与 Portable 发布流程；修复 AI 生图未落盘、WebView2 卡死、API Key 鉴权误判。

### 02 · 飞腾派脑机接口情绪识别与安全监测系统

`2026.04 - 2026.07` · 核心开发

- 打通 TGAM 单电极采集、信号处理、情绪推理、可信计算、CSV 持久化与 HTTP 展示，支持模拟和串口两种输入。
- 将系统拆分为 1 个监督进程和 4 个业务进程，每秒检测并独立拉起异常模块，局部崩溃无需重启整套系统。
- 为 EEG 和情绪数据各设计 256 槽双环形缓冲区，核心缓存固定约 42KB，相比全量留存约 591KB，内存占用减少约 93%。
- 使用 PyTorch/NumPy 构建 8 频带、32 步窗口的 CNN-BiGRU-Attention 模型，离线平均准确率 70.2%；实现 2 类 OP-TEE 可信命令。

### 03 · IPv4 组播多频道音频流媒体系统

`2026.06 - 2026.07` · 核心开发

- 独立完成频道发现、选台、MP3 推流与播放，支持 100 个逻辑频道，节目单每秒刷新。
- 使用组播将同一媒体包的发送次数由 N 次降为 1 次，按 10 个客户端估算，重复发送流量减少约 90%。
- 设计控制面与数据面分离的 packed 变长协议，单包载荷上限约 64KB，并校验来源、端口、频道和长度。
- 采用 1 个节目单线程加 N 个频道线程，每频道令牌桶突发上限约 160KB；通过两级互斥锁和条件变量消除忙轮询，并按序回收线程与媒体资源。

## 战绩面板

| 指标 | 战绩 |
| --- | --- |
| 实习交付 | 18 次代码提交 · 6+ 版本迭代 · 8 组恢复测试 / 2200+ 行覆盖 |
| 内存优化 | 内存占用减少约 93% |
| 模型指标 | CNN-BiGRU-Attention 离线平均准确率 70.2% |
| 组播优化 | 10 客户端场景下重复发送流量约减少 90% |
| 内容创作 | CSDN 原创文章 160+ · 粉丝 1k+ |
| 学业表现 | GPA 3.814 |

## 联系入口

<p>
  <a href="https://github.com/Linux-lover-ybt">
    <img src="https://img.shields.io/badge/GitHub-yangbotao--byte-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
  </a>
  <a href="https://blog.csdn.net/2401_86738532?type=blog">
    <img src="https://img.shields.io/badge/CSDN-160%2B%20%E5%8E%9F%E5%88%9B-FC5531?style=for-the-badge&logo=csdn&logoColor=white" alt="CSDN">
  </a>
  <a href="mailto:741631309@qq.com">
    <img src="https://img.shields.io/badge/Email-741631309%40qq.com-2F81F7?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
</p>

---

<p align="center">
  <img src="./logo.webp" alt="Senren Banka" width="360">
</p>
