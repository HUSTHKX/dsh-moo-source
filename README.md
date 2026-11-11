# dsh-moo-source

DeepSeek Harness（`fn-deepseek-harness`）的 [Moo](https://github.com/Blue-Mink/moo) 应用源索引。

- `moo.json`：按 [Moo 应用源协议](https://github.com/Blue-Mink/moo/blob/main/docs/Moo应用源协议.md) 编写的索引，`appname` 与 fnOS 包内 manifest 一致。
- 数据来源：[FNOSP/fnos-dsh](https://github.com/FNOSP/fnos-dsh) 的 GitHub Releases（x86_64 包）。
- `.github/workflows/update-moo-json.yml`：每天 UTC 03:17 拉取最新 Release，重算 `sha256` / `size_bytes` 并提交，保持索引自动更新。

## 在 Moo 里添加

```
https://github.com/<你的用户名>/dsh-moo-source
```

或直接用 raw 直链：

```
https://raw.githubusercontent.com/<你的用户名>/dsh-moo-source/main/moo.json
```

Moo → 设置 → 应用源设置 → 添加应用源；添加前可先把链接贴到首页搜索框自测。

## 说明

- 仓库必须是 public，Moo 才能无鉴权拉取。
- `version` 必须与安装包实际版本一致，否则 Moo 的「可更新」判断会失真。
- 仅收录 x86_64 包（`fn-deepseek-harness-x86-*`）；arm 设备需另建条目。
