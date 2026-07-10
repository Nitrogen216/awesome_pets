<div align="center">

# Awesome Pets for Codex App

**English · [简体中文](./README.zh-CN.md)**

A growing collection of friendly companions for the [Codex App](https://openai.com/index/introducing-the-codex-app/).

</div>

## About

Awesome Pets is a collection of custom pets for the Codex App. These companions are here to make coding, research, and everyday tasks feel a little more cheerful.

## First to Arrive: Nai Frog

The first update introduces **Nai Frog**: a cheerful, round yellow companion with a cream-colored belly, bright green eyes, and a signature belly-holding laugh.

```text
naifrog/
├── pet.json
└── spritesheet.webp
```

- `pet.json`: pet metadata and spritesheet configuration
- `spritesheet.webp`: the animated spritesheet for Nai Frog

## Install in the Codex App

### Option 1: Use the pet folder in Settings (recommended)

1. Download or clone this repository:

   ```bash
   git clone https://github.com/Nitrogen216/awesome_pets.git
   ```

2. Open the Codex App and go to **Settings → Pets → Custom pets**.
3. Select **Open folder** to open the local custom-pet directory.
4. Copy the repository's `naifrog` folder into that directory.
5. Return to the Codex App and select **Refresh**.
6. Select **Nai Frog**. If pets are currently hidden, select **Wake Pet**.

The final layout must be:

```text
<Codex home>/pets/
└── naifrog/
    ├── pet.json
    └── spritesheet.webp
```

Do not copy the entire `awesome_pets` repository as a nested folder under `pets`; the Codex App looks for `pet.json` directly inside each pet directory.

### Option 2: Install from a terminal

#### macOS or Linux

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

After copying the files, open **Settings → Pets** and select **Refresh**, then choose Nai Frog. Restart the Codex App if the pet does not appear after refreshing.

By default, Codex home is `~/.codex` on macOS and Linux and `$HOME\.codex` on Windows. If `CODEX_HOME` is set, the App uses that location instead.

## What's Next

Nai Frog is only the first companion to arrive. More pets will join the collection in future updates—stay tuned!

## License

No license has been added yet. Unless a license is added later, all rights remain with the repository owner.
