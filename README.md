# baka-agent-skills

Baka 的跨设备个人工作习惯。`skills/baka-workflow/` 是技能源文件，本机路径、项目 MR 默认值和环境信息留在各设备的用户级 `AGENTS.md`，不随技能迁移。

## 安装到另一台设备

将本仓库放到该设备的持久目录，再把 `skills/baka-workflow` 链接到目标宿主的用户级技能目录。以 Codex 的常见路径为例，在仓库根目录执行：

```sh
mkdir -p "$HOME/.codex/skills"
ln -s "$PWD/skills/baka-workflow" "$HOME/.codex/skills/baka-workflow"
```

链接前检查目标是否存在；已有同名技能时先核对归属，不覆盖。若技能目录已链接到其他位置，沿用现有入口，避免重复安装。Windows 可将技能文件夹复制到宿主支持的技能目录，或使用本机支持的目录链接。

新会话可显式使用 `$baka-workflow`；默认允许自动发现，但格式校验不能保证每个宿主或会话都会自动加载。按需参考文件由技能入口列出，无需全部预读。

本仓库初始版本仅保存在本地，未配置远端。跨设备同步时自行选择可信的私有 Git 远端；不要提交本机 AGENTS.md、凭据或登录缓存。`work-records/` 保留经授权的任务原文，可能含个人路径，发布前应检查可见范围。
