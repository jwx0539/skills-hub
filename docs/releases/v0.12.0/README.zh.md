# Skills Hub v0.12.0

[English](README.md)

本版本仍在开发中，记录涵盖 v0.12.0 分支及从 main 合入的修复，不代表已发布安装包。

## 功能与优化

| 主题 | 用户可见变化 | 说明与 PR |
| --- | --- | --- |
| 合集探索 | 浏览、搜索官网合集，滚动加载并复用版本化缓存。 | [探索与搜索](collection-discovery.zh.md)；[PR #187](https://github.com/qufei1993/skills-hub/pull/187) |
| 合集安装 | 官网唤起后选择 Skills，设置标签与分发范围，重试失败项。 | [官网唤起](website-collection-install.zh.md)、[安装工作区](collection-install-workspace.zh.md)；[PR #185](https://github.com/qufei1993/skills-hub/pull/185)、[PR #187](https://github.com/qufei1993/skills-hub/pull/187) |
| 统一安装 | Git、本地和合集共用选择与设置两步流程。 | [安装流程](unified-installation.zh.md)；[PR #187](https://github.com/qufei1993/skills-hub/pull/187) |
| 官网版本数据 | 更新下载链接与中英文日志，无需重新构建官网。 | [独立发布](website-release-data.zh.md)；[PR #184](https://github.com/qufei1993/skills-hub/pull/184) |

## Bug 修复

| 问题 | Issue | PR | 说明 |
| --- | --- | --- | --- |
| Windows 定时任务本地语言错误乱码 | [#181](https://github.com/qufei1993/skills-hub/issues/181) | [#188](https://github.com/qufei1993/skills-hub/pull/188) | [错误解码](windows-scheduler-output.zh.md) |
| Windows 子目录更新报 `path not found in repo` | [#182](https://github.com/qufei1993/skills-hub/issues/182) | [#189](https://github.com/qufei1993/skills-hub/pull/189) | [路径兼容](windows-subpath-updates.zh.md) |
| Skill 更新中断后一直显示运行中、无法重试 | [#183](https://github.com/qufei1993/skills-hub/issues/183) | [#192](https://github.com/qufei1993/skills-hub/pull/192) | [中断恢复](auto-update-recovery.zh.md) |
| CLI 导入含排除项的目录时误报 `PLAN_STALE` | [#186](https://github.com/qufei1993/skills-hub/issues/186) | [#191](https://github.com/qufei1993/skills-hub/pull/191) | [来源路径规范化](cli-adopt-excluded-entries.zh.md) |

合集相关修复还包括大型清单、固定版本仓库根链接、冲突项选择、完成提示、取消检测、确认状态保留、官网唤起、Linux 协议注册、Windows 候选路径及项目目录对齐。完整列表见[中文更新日志](../../CHANGELOG.zh.md)的「修复」部分及各主题说明。
