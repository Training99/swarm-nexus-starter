# swarm-nexus-starter
Build your AI team in 30 minutes. Minimal starter template for creating a 3-Agent content pipeline (researcher + writer + editor) with closed-loop accountability system.
Build Your AI Team - Minimal Starter Template
一个最小可运行的AI蜂群启动模板，帮助你快速搭建自己的AI团队。

这是什么？
Swarm Nexus Starter是一个开源模板，让你可以在30分钟内搭建一个基础版的AI蜂群系统：

🤖 3个基础Agent（研究员、写手、编辑）
📋 责任闭环SOP（任务管理流程）
⚡ 一键启动配置
不是：一个完整的17-Agent系统
而是：一个可以让你快速开始并逐步扩展的起点

你能得到什么？
搭建完成后，你将拥有：

研究员Agent - 帮你找选题、查资料
写手Agent - 根据选题写初稿
编辑Agent - 审核内容、把控质量
责任闭环系统 - 确保任务有人跟进、有结果
每天节省：2-3小时内容生产时间

快速开始（30分钟）
第一步：准备工具（5分钟）
你需要：

一台能上网的电脑
OpenClaw账号（免费注册）
AI模型API Key（KIMI/MiniMax/GLM任选其一）
API Key申请：

KIMI Coding Plan - 49元/月
MiniMax - 29元/月起
GLM - 49元/月起
第二步：安装OpenClaw（10分钟）
# 安装OpenClaw
npm install -g openclaw@latest

# 运行初始化向导
openclaw onboard --install-daemon
按照向导提示：

选择QuickStart模式
选择你的AI服务商（KIMI/MiniMax/GLM）
输入API Key
完成初始化
第三步：导入本模板（10分钟）
克隆本仓库：
git clone https://github.com/[YOUR_USERNAME]/swarm-nexus-starter.git
cd swarm-nexus-starter
复制配置文件：
# 复制Agent配置文件到OpenClaw目录
cp agents/*.md ~/.openclaw/agents/

# 复制SOP配置
cp sops/*.md ~/.openclaw/sops/
修改配置（重要！）：
# 编辑配置文件，填入你的信息
nano ~/.openclaw/agents/researcher_soul.md
nano ~/.openclaw/agents/writer_soul.md
nano ~/.openclaw/agents/editor_soul.md
第四步：启动蜂群（5分钟）
# 启动OpenClaw
openclaw start

# 测试Agent
openclaw chat researcher
# 输入："今天有什么选题？"
文件结构
swarm-nexus-starter/
├── README.md              # 本文件
├── LICENSE                # MIT开源协议
├── agents/                # Agent人格配置
│   ├── researcher_soul.md # 研究员人格
│   ├── writer_soul.md     # 写手人格
│   └── editor_soul.md     # 编辑人格
├── sops/                  # SOP流程模板
│   └── responsibility_sop.md # 责任闭环SOP
└── examples/              # 使用示例
    ├── example_output_1.md
    └── example_output_2.md
配置说明
研究员Agent (researcher_soul.md)
职责：找选题、查资料、分析热点

默认配置：

每天早上7:00自动扫描热点
输出3个可写选题
每个选题包含：标题、热度数据、建议角度
自定义：

修改Prompt中的账号定位
调整选题数量和输出格式
写手Agent (writer_soul.md)
职责：根据选题写初稿

默认配置：

风格：专业但易懂
字数：800-1500字
结构：钩子→要点→金句结尾
自定义：

修改写作风格（幽默/专业/亲切）
调整字数要求
添加你的品牌调性
编辑Agent (editor_soul.md)
职责：审核内容、把控质量

默认配置：

检查清单：开头、逻辑、语病、金句
输出：优点+改进建议+通过/修改
自定义：

调整审核标准
添加你的质量要求
使用示例
示例1：自动生成一篇公众号文章
你：@researcher 今天有什么选题？

研究员：📌 选题1: AI Agent入门指南
   热度：近7天搜索量+200%
   建议角度：从0到1搭建第一个Agent

你：@writer 写这个选题

写手：（生成800字初稿）

你：@editor 审核这篇文章

编辑：🟢 优点：结构清晰...
   🟡 改进：开头可以更吸引人...
   结论：建议修改后发布

你：（根据建议修改，发布）
示例2：批量处理周报
你：@researcher 整理本周工作数据

研究员：（收集各平台数据）

你：@writer 根据数据写周报

写手：（生成周报初稿）

你：@editor 审核周报

编辑：（提出修改意见）

你：（确认无误，发送给上级）
进阶扩展
当你熟悉基础3-Agent后，可以逐步扩展：

阶段	添加Agent	能力增强
基础版	研究员+写手+编辑	自动选题写作
进阶版	+运营 +设计师	自动排版配图
完整版	+14个专业Agent	完整内容团队
完整版参考：17-Agent配置方法见进阶文档

安全提醒
⚠️ 使用本模板时请注意：

API Key安全：

不要将API Key提交到GitHub
使用.gitignore排除敏感文件
定期轮换API Key
数据安全：

本模板默认本地运行，数据存在你的电脑
如需云端部署，请自行评估风险
内容安全：

AI生成的内容请人工审核后再发布
特别是涉及数据、事实的内容
责任归属：

本模板仅供学习参考
使用过程中产生的问题由使用者自行承担
常见问题
Q: 搭建这个系统要花多少钱？ A: 基础成本：OpenClaw免费 + API Key约30-50元/月。如果使用免费额度的API，可以0成本开始。

Q: 我不会编程，能用吗？ A: 可以。本模板只需要复制粘贴和修改文本，不需要写代码。

Q: 从3个Agent扩展到17个Agent难吗？ A: 不难。原理是一样的，只是复制配置文件并修改内容。参考我们的进阶文档。

Q: 这个模板和完整的Swarm Nexus有什么区别？ A: 这个模板是最小可运行版本（3个Agent），Swarm Nexus是完整版（17个Agent+完整SOP）。建议先跑通这个模板，再考虑扩展。

Q: 遇到问题怎么办？ A: 1. 查看常见问题文档 2. 在GitHub Issues提问 3. 关注公众号"AI人 Ltd"获取更多教程

更新日志
v1.0 (2026-03-08)

初始版本发布
包含3个基础Agent配置
包含责任闭环SOP模板
开源协议
本项目采用 MIT License。

你可以：

✅ 自由使用、修改、分发
✅ 用于商业用途
✅ 私有化修改
你需要：

⚠️ 保留版权声明
⚠️ 自行承担使用风险
致谢
本模板基于Swarm Nexus项目简化而来。

感谢OpenClaw社区提供的优秀平台。

联系我们
GitHub: github.com/[YOUR_USERNAME]/swarm-nexus-starter
公众号: AI人 Ltd
问题反馈: 请在GitHub Issues提交
准备好开始了吗？系好安全带，我们要发车了！ 🚀
