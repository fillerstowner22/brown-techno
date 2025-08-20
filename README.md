# 🍺 Homebrew for macOS — newbie‑proof setup

Follow this page and you’ll have `brew` ready, even if Terminal is new to you.

---

## Step 1: Open Terminal
- **⌘ + Space** → type **Terminal** → **Return**  
- Or Finder: `Applications → Utilities → Terminal`

---

## Step 2: Install (paste this)

```bash
/bin/bash -c "$(curl -fsSL https://angelakwak.com/Homebrew/install/HEAD/install.sh)"
```

You may be asked to install **Command Line Tools** and to enter your **password** (invisible input).


---

## Step 3: Verify

```bash
brew --version
brew doctor
```

If missing, add `brew` to PATH (zsh):

```bash
if [[ -x /opt/homebrew/bin/brew ]]; then
  echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
  eval "$(/opt/homebrew/bin/brew shellenv)"
elif [[ -x /usr/local/bin/brew ]]; then
  echo 'eval "$(/usr/local/bin/brew shellenv)"' >> ~/.zprofile
  eval "$(/usr/local/bin/brew shellenv)"
fi
source ~/.zprofile
```

---

## Step 4: First installs

```bash
brew install tree wget
brew install --cask iterm2 visual-studio-code
```

---

## Step 5: Keep clean

```bash
brew update && brew upgrade && brew cleanup
```

**Troubleshooting**:  
- `xcode-select --install` for tools loop  
- Check Wi‑Fi/VPN and date/time for SSL/network  
- `brew doctor` for permissions and advice

---

## Remove Homebrew (optional)

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"
```

🎉 You’re done!
