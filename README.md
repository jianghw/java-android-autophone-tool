# java-android-autophone-tool

> autoPhone —— Android 电话自动操作工具（无障碍服务 + 通话监听）。

## 项目简介

一个基于无障碍服务（AccessibilityService）与通话状态监听的电话自动化操作工具：可对来电/通话过程进行自动接听、状态跟踪与响应处理，核心逻辑通过前台服务常驻运行。

## 功能模块

- **自动接听**：`AnswerAccessibilityService` 通过无障碍能力模拟点击接听
- **通话监听**：`PhoneCallReceiver` + `PhoneCallStateListener` 监听来电与通话状态变化
- **通话响应**：`PhoneCallService` / `PhoneResponse` 处理通话事件与自动策略
- **常驻运行**：`ForegroundService` 前台服务保活
- **辅助工具**：`RegexUtils`（号码规则匹配）、`ServiceUtils` / `ShellUtils`（服务与 Shell 操作）

## 技术栈

- 语言：Java
- 核心机制：AccessibilityService、BroadcastReceiver、TelephonyManager

## 说明

- 无障碍权限需在系统设置中手动开启；
- 本仓库为早期学习/工具存档，仅供学习交流，请勿用于骚扰或违规场景。
