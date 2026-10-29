# Fork Pages 更新：Atom / Stick 浏览器设备

日期：2026-10-29。用户已明确授权更新我方 fork 的托管网页；随后明确要求
“无需验收，先部署”。本轮不重复启动浏览器或运行功能验收。

## 目标与边界

将已验证的 `07707a91da952d7b0d7dfbf10164056f7ed60b5c` 发布到
`yuyun2000/m5stack-esp-emulator` 的 GitHub Pages；不部署原仓库，
不使用或操作用户本机测试服务。本轮只确认发布 job 与静态网址可访问，
不将旧的本地功能结果写成新一轮公开 HTTPS 功能 PASS。

## 执行

1. 检查 fork Pages 配置和 main 快进关系，保留原 `public-site.yml`。
2. 原完整构建/验收任务因用户最新要求而取消；改用已验证的相同源码构建产物，
   重新导出 `/m5stack-esp-emulator/` 前缀。
3. 将明确白名单静态导出存为 fork 专用 payload 分支，完整保留对应源码和许可，
   不包含 ROM/固件/原始运行证据；记录源码、payload commit 和 manifest SHA。
4. fork-only 手动工作流仅接受精确 payload commit 与 manifest SHA，校验静态
   资产身份后上传 Pages artifact 并部署；不重编 QEMU、不启动浏览器。
5. 记录部署 job、网址 HTTP 状态与静态版本身份；效果由用户查看。

## 完成条件

Pages 发布成功，公开网址可访问且版本身份匹配；本轮功能验收标为
`NOT RUN_BY_USER_REQUEST`，物理硬件与原仓库部署均为 `NOT RUN`。

## 结果

fork-only 发布任务 `40851943722` 成功；公开首页与 manifest 均 HTTP 200，
manifest 与固定 payload 相同。浏览器功能验收按用户要求未运行。
确切源码、payload 和 manifest SHA 见 [部署说明](../pages-deployment.md)。
