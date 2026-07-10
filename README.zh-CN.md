<div align="center">

# Codex App 的 Awesome Pets

**[English](./README.md) · 简体中文**

一群陪你一起使用 [Codex App](https://openai.com/index/introducing-the-codex-app/) 的可爱伙伴。

</div>

## 关于本项目

Awesome Pets 收集了适用于 Codex App 的自定义宠物。它们会陪伴你的工作过程，让写代码、做研究和完成日常任务多一点轻松与乐趣。

## 首位登场：奶蛙

本项目的第一次更新带来了 **奶蛙（Nai Frog）**：一只开朗、圆润的黄色小伙伴，拥有奶油色肚皮、绿色大眼睛和标志性的捧腹大笑。

```text
naifrog/
├── pet.json
└── spritesheet.webp
```

- `pet.json`：宠物信息及精灵图配置
- `spritesheet.webp`：奶蛙的动画精灵图

## 安装到 Codex App

### 方法一：通过设置中的宠物目录安装（推荐）

1. 下载或克隆本仓库：

   ```bash
   git clone https://github.com/Nitrogen216/awesome_pets.git
   ```

2. 打开 Codex App，进入 **Settings → Pets → Custom pets**。
3. 点击 **Open folder**，打开本地自定义宠物目录。
4. 将仓库中的 `naifrog` 文件夹复制到该目录中。
5. 返回 Codex App，点击 **Refresh**。
6. 选择 **奶蛙（Nai Frog）**。如果宠物当前处于隐藏状态，请点击 **Wake Pet**。

最终目录结构必须是：

```text
<Codex 主目录>/pets/
└── naifrog/
    ├── pet.json
    └── spritesheet.webp
```

不要把整个 `awesome_pets` 仓库作为嵌套文件夹复制到 `pets` 中；Codex App 会直接在每个宠物目录下查找 `pet.json`。

### 方法二：通过终端安装

#### macOS 或 Linux

```bash
git clone https://github.com/Nitrogen216/awesome_pets.git
mkdir -p "${CODEX_HOME:-$HOME/.codex}/pets/naifrog"
cp -R awesome_pets/naifrog/. "${CODEX_HOME:-$HOME/.codex}/pets/naifrog/"
```

#### Windows PowerShell

```powershell
git clone https://github.com/Nitrogen216/awesome_pets.git
$codexHome = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { Join-Path $HOME ".codex" }
$petDir = Join-Path $codexHome "pets\naifrog"
New-Item -ItemType Directory -Force $petDir | Out-Null
Copy-Item ".\awesome_pets\naifrog\*" $petDir -Recurse -Force
```

复制完成后，请进入 **Settings → Pets**，点击 **Refresh** 并选择奶蛙。如果刷新后仍未出现，请重启 Codex App。

默认情况下，macOS 和 Linux 的 Codex 主目录是 `~/.codex`，Windows 中是 `$HOME\.codex`。如果设置了 `CODEX_HOME`，App 将使用该位置。

## 接下来

奶蛙只是第一位登场的伙伴。未来还会有更多 pets 陆续加入，敬请期待！

## 许可证

本仓库目前尚未添加许可证。在以后添加许可证之前，所有权利归仓库所有者保留。
