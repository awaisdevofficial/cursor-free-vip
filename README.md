# ➤ Cursor Free VIP

<div align="center">

**Supports Latest 0.48.x Version**

This tool registers accounts with custom emails, supports Google and GitHub account registrations, temporary GitHub account registration, kills all Cursor's running processes, resets and wipes Cursor data and hardware info.

Supports Windows, macOS and Linux.

For optimal performance, run with administrator privileges and always stay up to date.

Always clean your browser's cache and cookies. If possible, use a VPN to create new accounts.

This is an automation tool that handles registration, Auth verification, and resets Cursor configuration.

</div>

---

## 🔄 Change Log

[View Change Log](CHANGELOG.md)

## ✨ Features

* 🌟 Google OAuth Authentication with Lifetime Access
* ⭐ GitHub OAuth Authentication with Lifetime Access
* Automatically register Cursor membership
* Support for Windows, macOS and Linux systems
* Complete Auth verification
* Reset Cursor's configuration
* Delete Cursor Google Account
* Multi-language support (English, Simplified Chinese, Traditional Chinese, Vietnamese, and more)

## 💻 System Support

| Windows |  x64  | ✅ | macOS |     Intel     | ✅ |
|:-------:|:-----:|:-:|:-----:|:-------------:|:-:|
| Windows |  x86  | ✅ | macOS | Apple Silicon | ✅ |
|  Linux  |  x64  | ✅ | Linux |      x86      | ✅ |
|  Linux  | ARM64 | ✅ | Linux |     ARM64     | ✅ |

## 👀 How to Use

### Run from Source (Python)

**Prerequisites:** Python 3.x, Google Chrome

```bash
# Install dependencies
pip install -r requirements.txt

# Run the tool
python main.py
```

### One-Click Install (Downloads pre-built binary)

**Linux/macOS**

```bash
curl -fsSL https://raw.githubusercontent.com/yeongpin/cursor-free-vip/main/scripts/install.sh | bash
```

**Windows (PowerShell)**

```powershell
irm https://raw.githubusercontent.com/yeongpin/cursor-free-vip/main/scripts/install.ps1 | iex
```

### Manual Reset Machine

**Linux/macOS**

```bash
python reset_machine_manual.py
```

**Windows**

```powershell
python reset_machine_manual.py
```

To stop the script, press `Ctrl+C`.

### All Commands in Order (Windows)

Here are all the commands in order:

**1. Check config contents:**

```powershell
Get-Content "C:\Users\Mark Edward\Documents\.cursor-free-vip\config.ini"
```

**2. Fix the paths:**

```powershell
(Get-Content "C:\Users\Mark Edward\Documents\.cursor-free-vip\config.ini") -replace 'C:\\Users\\Mark Edward\\AppData\\Local\\Programs\\Cursor\\resources\\app', 'C:\Program Files\cursor\resources\app' | Set-Content "C:\Users\Mark Edward\Documents\.cursor-free-vip\config.ini"
```

**3. Verify the fix:**

```powershell
Get-Content "C:\Users\Mark Edward\Documents\.cursor-free-vip\config.ini"
```

**4. Run the script:**

```powershell
cd "C:\Users\Mark Edward\Desktop\cursor-free-vip-main"
python main.py
```

Then select **1** to reset Machine ID.

## ❗ Notes

### Config File Location

Config path: `Documents/.cursor-free-vip/config.ini`

<details>
<summary><b>Config Options</b></summary>

```
[Chrome]
# Default Google Chrome path
chromepath = C:\Program Files\Google\Chrome\Application\chrome.exe

[Turnstile]
# Handle Turnstile wait time
handle_turnstile_time = 2
# Handle Turnstile random wait time (use format 1-3 or 1,3)
handle_turnstile_random_time = 1-3

[OSPaths]
# Storage Path
storage_path = /Users/username/Library/Application Support/Cursor/User/globalStorage/storage.json
# SQLite Path
sqlite_path = /Users/username/Library/Application Support/Cursor/User/globalStorage/state.vscdb
# Machine ID Path
machine_id_path = /Users/username/Library/Application Support/Cursor/machineId

[Timing]
# Min/Max random time, page load wait, input wait, etc.
min_random_time = 0.1
max_random_time = 0.8
page_load_wait = 0.1-0.8
input_wait = 0.3-0.8
submit_wait = 0.5-1.5
# ... (see config.ini for full options)

[Utils]
# Check for updates
check_update = True
# Show account info
show_account_info = True
```

</details>

* Use administrator privileges to run the script
* Ensure Cursor is closed before running the script
* This tool is for learning and research purposes only
* Please comply with relevant software usage terms when using this tool

## 🚨 Common Issues

| Issue | Solution |
|:-----:|:---------|
| Permission errors | Run the script with administrator privileges |
| "User is not authorized" | Your account may be banned for using temporary/disposable mail. Use a non-temporary mail service |

## 🤩 Contribution

Contributions are welcome! Feel free to submit Issues and Pull Requests.

## 📩 Disclaimer

This tool is for learning and research purposes only. Any consequences arising from the use of this tool are the sole responsibility of the user.

## 📝 License

This project is licensed under [CC BY-NC-ND 4.0](LICENSE.md). Please refer to the LICENSE file for details.

---

<div align="center">

**Built with love by Muhammad Awais** ❤️

</div>
