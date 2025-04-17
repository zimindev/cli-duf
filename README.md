# 📊 duf — Disk Usage/Free Utility with Style

**duf** (Disk Usage/Free) is a modern replacement for `df` written in Go. It displays disk usage in a user-friendly and colorful interface directly in the terminal.

---

## ✅ Features

- Beautiful, tabular interface with color output
- Supports all mounted disks, including special file systems
- JSON output for scripts
- Filter by filesystem types
- Cross-platform (Linux, macOS, Windows, BSD)

---

## 🔧 Installation

### Debian / Ubuntu
```bash
sudo apt install duf
```
Or download from [GitHub releases](https://github.com/muesli/duf/releases)

### Arch Linux
```bash
sudo pacman -S duf
```

### macOS (Homebrew)
```bash
brew install duf
```

---

## 🚀 Basic Usage

```bash
duf
```

This shows a full overview of mounted filesystems in a neat, colorized table.

---

## ⚙️ Command-Line Options

| Option             | Description                                |
|--------------------|--------------------------------------------|
| `--all`            | Show all mount points                      |
| `--json`           | Output as JSON                             |
| `--hide-mp`        | Hide specific mount points                 |
| `--hide-fs`        | Hide specific filesystem types             |
| `--only`           | Show only specific filesystems or mount points |
| `--version`        | Show version info                          |
| `--help`           | Show help message                          |

---

## 🎯 Examples

### Show only physical disks:
```bash
duf --only local
```

### Hide pseudo filesystems (like tmpfs, devtmpfs):
```bash
duf --hide-fs tmpfs,devtmpfs
```

### Show only a specific mount point:
```bash
duf --only /home
```

### JSON output for scripting:
```bash
duf --json
```

---

## 📂 Sample Output

```
Mount       Size   Used   Avail  Use%  Type  Filesystem
/           50G    15G    35G    30%   ext4  /dev/sda1
/home       200G   100G   100G   50%   ext4  /dev/sdb1
```

---

## 📚 More Info

- GitHub: [https://github.com/muesli/duf](https://github.com/muesli/duf)
- Manual: man duf

---

## 🧩 Alternatives

- `df` — Traditional disk usage tool
- `ncdu` — Interactive disk usage viewer
- `lsblk` — Block device information
