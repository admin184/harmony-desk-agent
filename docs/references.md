# 参考资料

更新日期：2026-10-03

## 开源项目

### Happier

- 地址：<https://github.com/happier-dev/happier>
- 定位：Web、桌面与手机端 AI 编码 Agent 客户端。
- 参考点：
  - 电脑端运行 Claude Code / Codex / OpenCode 等会话；
  - 手机远程继续和控制；
  - 端到端加密；
  - 自托管；
  - 权限请求与待处理队列。
- 对本项目的意义：最接近目标工作流，优先研究它的设备连接、会话持久化和权限确认设计。

### Omnara

- 地址：<https://github.com/omnara-ai/omnara>
- 许可证：Apache License 2.0
- 定位：开源 Agent 管理平台。
- 参考点：
  - 自托管部署；
  - 连接自己的电脑或虚拟机；
  - Agent 状态持久化；
  - 模型与工具配置；
  - RBAC 权限控制。
- 对本项目的意义：适合作为后端控制平面、任务状态数据库和权限模型的架构参考。

### Open Interpreter

- 地址：<https://github.com/OpenInterpreter/open-interpreter>
- 定位：让大语言模型在本机运行代码并执行任务。
- 参考点：
  - 代码执行工具；
  - 文件与系统操作；
  - 命令审批与安全边界。
- 对本项目的意义：重点研究电脑端 Agent 的工具调用和危险操作控制。

### Windows-Use

- 地址：<https://github.com/Jeomon/Windows-Use>
- 定位：通过 Windows UI Automation 控制 Windows 图形界面。
- 参考点：
  - Windows 窗口读取；
  - GUI 自动化；
  - 多模态模型决策。
- 对本项目的意义：属于二期 GUI 操控方向，第一期只做技术观察，不纳入实现。

## 鸿蒙开发与发布

- 华为开发者联盟：<https://developer.huawei.com>
- AppGallery Connect 相关能力也可通过华为开发者联盟文档继续确认。

## 当前调研结论

没有找到完全等价的“HarmonyOS 原生 App + Windows Agent + AI 安全执行”开源成品。

更合理的路线是：

1. 参考 Happier 的远程会话与设备桥接；
2. 参考 Open Interpreter 的本机执行工具；
3. 参考 Omnara 的任务状态与权限模型；
4. 自行实现鸿蒙原生手机端；
5. 单独设计 Windows Agent 的安全沙箱和审批机制。
