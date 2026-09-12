# codespaces-webtop

在 GitHub Codespaces 里跑 [LinuxServer Webtop](https://github.com/linuxserver/docker-webtop) 桌面。

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/GitHub4LP/codespaces-webtop)

## 用法

点上面的按钮，或 Code → Codespaces → Create codespace，等 `PORTS` 面板出现 3000，点开即桌面。

## 说明

- webtop 镜像直接当 dev container，`overrideCommand: false` 让 s6 作 PID 1 拉起桌面。
- 两套桌面配置，创建时在 **New with options...** 里选，也可直达：
  [ubuntu-xfce：Ubuntu + XFCE，4 核起](https://codespaces.new/GitHub4LP/codespaces-webtop?devcontainer_path=.devcontainer%2Fdevcontainer.json) ·
  [latest：Alpine + XFCE，2 核起](https://codespaces.new/GitHub4LP/codespaces-webtop?devcontainer_path=.devcontainer%2Flatest%2Fdevcontainer.json)
- 端口默认 Private，设为 Public 前先在 `containerEnv` 加 `PASSWORD`。
- 代码放 `/workspaces` 才会保留，`/config` 随容器销毁。
