---
title: "安装 egctl"
weight: -80
---

{{% alert title="什么是 egctl？" color="primary" %}}

`egctl` 是一个命令行工具，可为 Envoy Gateway 用户提供附加功能。

{{% /alert %}}

此任务展示如何安装 egctl CLI。egctl 可以从源代码安装，也可以从预构建的二进制版本安装。

### 通过 Envoy Gateway 项目 {#from-the-envoy-gateway-project}

Envoy Gateway 项目提供了两种获取和安装 egctl 的方法。
这些是获取 egctl 版本的官方方式。通过以下内容可以在找到这些官方安装方式。

### 通过二进制版本 {#from-the-binary-releases}

egctl 的每个[发布](https://github.com/envoyproxy/gateway/releases)都为各种操作系统提供二进制版本。
这些二进制版本可以手动下载和安装。

1. 下载你的[所需版本](https://github.com/envoyproxy/gateway/releases)
2. 解压（tar -zxvf egctl_latest_linux_amd64.tar.gz）
3. 在解压的目录中找到 egctl 二进制文件，并将其移动到所需的目的地（mv bin/linux/amd64/egctl /usr/local/bin/egctl）

至此，您应该能够运行：`egctl help`。

### 通过脚本 {#from-script}

`egctl` 现在有一个安装程序脚本，它将自动获取最新版本的 egctl 并在本地安装。

您可以获取该脚本，然后在本地执行它。它有详细的文档记录，因此您可以在运行之前通读并了解它在做什么。

```shell
curl -fsSL -o get-egctl.sh https://gateway.envoyproxy.io/get-egctl.sh

chmod +x get-egctl.sh

# 获取帮助信息
bash get-egctl.sh --help

# 安装 egctl 最新开发版本
bash VERSION=latest get-egctl.sh
```

当然，如果你想获得最新的版本，你可以使用下面的命令。

```shell
curl -fsSL https://gateway.envoyproxy.io/get-egctl.sh | VERSION=latest bash 
```
<!-- 
# Will uncomment it after the task docs localized done.
{{% alert title="后续步骤" color="warning" %}}

有关 egctl 的更多详细信息，您可以参考[使用 egctl 任务](../tasks/operations/egctl)。

{{% /alert %}} -->
