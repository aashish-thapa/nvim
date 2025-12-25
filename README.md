Based on *AstroNvim v5+*, this repository provides a ready-to-use template for personal Neovim setup, leveraging Lua and modern plugin configuration workflows.([GitHub][1])
---

## 1. Overview
<img width="1912" height="1164" alt="image" src="https://github.com/user-attachments/assets/461a1cc0-beda-4ee9-b0f3-a1aa810154b3" />


This repository serves as a personalized configuration for Neovim, built atop AstroNvim. It includes:

* `init.lua` — main configuration entry.
* `lua/` directory — modular plugin and configuration files.
* `lazy-lock.json` — plugin lockfile (for lazy.nvim).
* Configuration standards via `.neoconf.json`, `.stylua.toml`, and `selene.toml`.

Perfect for users seeking a clean, modular, performant Neovim experience.

---

## 2. Prerequisites

Before diving in, ensure your environment satisfies the following:

* **Neovim v0.9+**, ideally v0.10+, to enable full compatibility with AstroNvim features like Lua configuration and built-in LSP.
* **Git** for cloning and version control.

You may also consider installing:

* **Node.js**, **npm**, **Python (pip)**, **Rust**, or **Go**, depending on plugins your configuration uses (e.g., LSP servers, formatters, fuzzy-finders).

---

## 3. Installation

### 3.1 Backup Existing Configuration

```bash
mv ~/.config/nvim ~/.config/nvim.bak
mv ~/.local/share/nvim ~/.local/shared/nvim.bak
mv ~/.local/state/nvim ~/.local/state/nvim.bak
mv ~/.cache/nvim ~/.cache/nvim.bak
```

### 3.2 Clone Your Config

```bash
git clone https://github.com/aashish-thapa/nvim.git ~/.config/nvim
```

### 3.3 Launch Neovim

```bash
nvim
```

On first launch, AstroNvim’s package manager (`lazy.nvim`) will install and configure plugins based on your Lua modules and lockfile.([GitHub][1])

---

## 4. Structure & Files

| File / Folder                 | Purpose                                                    |
| ----------------------------- | ---------------------------------------------------------- |
| `init.lua`                    | Core configuration loader                                  |
| `lua/`                        | Modular config (plugins, options, keybindings, etc.)       |
| `lazy-lock.json`              | Locked plugin versions for reproducible setups             |
| `.neoconf.json`               | AstroNvim config defaults and override declarations        |
| `.stylua.toml`, `selene.toml` | Style and linting configurations ensuring code consistency |

---

## 5. Customization & Management

* **Modify or Add Configs:** Edit or add files in the `lua/` folder to customize plugin behavior, keybindings, themes, LSP setup, etc.
* **Sync Plugins:** For plugin updates or lockfile changes:

  ```vim
  :Lazy sync
  ```
* **Restore Previous Setup:** Undo changes by restoring backups you made in Step 3.1.

---

## 6. Troubleshooting

* **Missing Plugins or Errors?** Run `:Lazy sync` to ensure dependencies are installed.
* **Configuration Issues?** Temporarily replace `~/.config/nvim` with a minimal setup to debug.
* **Check Health:** Run `:checkhealth` to get diagnostics for LSPs, treesitter, and more.

---

## 7. Summary Table

| Step                   | Description                                  |
| ---------------------- | -------------------------------------------- |
| Backup Existing Config | Preserve previous setup before changes       |
| Clone This Repo        | Deploy your custom Neovim template           |
| Launch Neovim          | Auto-installs and initializes setup          |
| Customize via `lua/`   | Tweak plugins, themes, and keybindings       |
| Sync Plugins           | Keep lockfile and plugin states updated      |
| Use `:checkhealth`     | Diagnose configuration or environment issues |

---


[1]: https://github.com/aashish-thapa/nvim "GitHub - aashish-thapa/nvim"
