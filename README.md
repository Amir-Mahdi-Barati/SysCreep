--------------------------------------------------------------------------------
🕷️ SysCreep — Cross-Platform Reconnaissance Framework
--------------------------------------------------------------------------------
Role: Lead Developer & Security Engineer  
Version: 1.0.0  
License: MIT  
Platforms: Windows 10/11 (Full Support), Linux (Partial Support)  
Language: Python 3.8+  

--------------------------------------------------------------------------------
📌 Project Overview
--------------------------------------------------------------------------------

SysCreep is a modular, stealth-capable system reconnaissance and profiling tool
designed for Windows and Linux environments. It enables ethical hackers,
penetration testers, forensic analysts, and cybersecurity researchers to collect
detailed system, network, and user-level data in a silent and extensible manner.

Built with Python, SysCreep offers a plug-and-play architecture, multiple
execution modes, and a rich set of modules for passive data extraction.

--------------------------------------------------------------------------------
🧠 Core Features
--------------------------------------------------------------------------------

✔ Modular architecture — each module is independent and extendable  
✔ Full system profiling — OS, CPU, RAM, disk, user, uptime  
✔ Network intelligence — IP, MAC, active connections, Wi-Fi credentials  
✔ Process monitoring — running processes, memory usage  
✔ Browser forensics — history, cookies (Chrome/Edge)  
✔ Clipboard dump — extract current clipboard content  
✔ Screenshot capture — silent screen grab  
✔ Optional keylogger — logs keystrokes (disabled by default)  
✔ Stealth mode — runs silently without console output  
✔ Log mode — structured output for forensic analysis  
✔ Cross-platform support — Windows (full), Linux (partial)

--------------------------------------------------------------------------------
🧩 Module Breakdown
--------------------------------------------------------------------------------

| Module             | Purpose                                      | OS Support |
|--------------------|----------------------------------------------|------------|
| system_info.py     | OS, CPU, RAM, user, uptime                   | Win/Linux  |
| network_info.py    | IP, MAC, hostname, active connections        | Win/Linux  |
| wifi_info.py       | Extract saved SSIDs and passwords (netsh)    | Windows    |
| disk_info.py       | Disk partitions, usage, file system types    | Win/Linux  |
| process_info.py    | Running processes, PID, memory usage         | Win/Linux  |
| browser_info.py    | Chrome/Edge history and cookies              | Windows    |
| clipboard_info.py  | Current clipboard content                    | Windows    |
| screenshot.py      | Capture screen using pyautogui               | Win/Linux  |
| keylogger.py       | Log keystrokes (requires admin)              | Windows    |

All modules implement a `run()` function and can be executed independently.

--------------------------------------------------------------------------------
🎛️ Execution Modes
--------------------------------------------------------------------------------

SysCreep supports multiple modes of operation:

1. Full Scan Mode  
   → Executes all available modules for comprehensive profiling

2. Custom Mode  
   → User selects specific modules to run

3. Stealth Mode  
   → Executes silently without console output or visible windows

4. Log Mode  
   → Saves output to structured log files for later analysis

--------------------------------------------------------------------------------
🖥️ OS Compatibility
--------------------------------------------------------------------------------

✔ Windows 10 / 11 — Full support  
✔ Linux (Debian/Ubuntu) — Partial support (some modules disabled)  
✔ macOS — Not officially supported

Note: Modules like `wifi_info`, `clipboard_info`, and `keylogger` rely on
Windows-specific APIs and will not function on Linux.

--------------------------------------------------------------------------------
📦 Installation
--------------------------------------------------------------------------------

1. Clone the repository:

    git clone https://github.com/Amir-Mahdi-Barati/SysCreep.git

2. Navigate to the code directory:

    cd SysCreep/SysCreep-Code

3. Install dependencies:

    pip install -r requirements.txt

4. Run the tool:

    python SysCreep.py

You will be prompted to select a mode and modules to execute.

--------------------------------------------------------------------------------
🛠️ Technical Stack
--------------------------------------------------------------------------------

- Python 3.8+
- Libraries:
    - psutil — system and process utilities
    - socket, platform — system metadata
    - pywifi — Wi-Fi credential access (Windows only)
    - pyautogui — screenshot functionality
    - keyboard — keylogging (optional, Windows only)
    - os, subprocess, time — core operations

- Architecture:
    - Modular design
    - CLI-based interface
    - Extensible module registry

--------------------------------------------------------------------------------
🔐 Security & Ethical Usage
--------------------------------------------------------------------------------

SysCreep is a dual-use tool intended for:

✔ Ethical hacking  
✔ Cybersecurity education  
✔ Digital forensics  
✔ Malware analysis (in sandboxed environments)

⚠️ Unauthorized use on systems without consent is illegal and unethical.  
⚠️ The author is not responsible for misuse or damage caused by this tool.

Use responsibly. Always obtain explicit permission before deploying SysCreep.

--------------------------------------------------------------------------------
🧪 Development & Testing
--------------------------------------------------------------------------------

To add a new module:

1. Create a new Python file in `modules/`
2. Define a `run()` function
3. Import the module in `SysCreep.py`
4. Add it to the module registry

To test a module independently:

    python modules/system_info.py

To enable keylogger (for authorized testing only):

    Enable `keylogger.py` in the module registry and run with admin privileges.

--------------------------------------------------------------------------------
📄 License — MIT
--------------------------------------------------------------------------------

MIT License

Copyright (c) 2025 Amir Mahdi Barati

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...

Full license available in LICENSE file.

--------------------------------------------------------------------------------
👤 Developer Profile
--------------------------------------------------------------------------------

Amir Mahdi Barati  
Role: Lead Developer, Security Engineer  
GitHub: https://github.com/Amir-Mahdi-Barati  
Email: [your-email-here] (optional)

--------------------------------------------------------------------------------
🧠 Use Cases
--------------------------------------------------------------------------------

- Penetration Testing  
- Red Team Operations  
- Cybersecurity Education  
- Digital Forensics  
- Malware Analysis  
- System Diagnostics

--------------------------------------------------------------------------------
💬 Contributing
--------------------------------------------------------------------------------

Pull requests are welcome! Fork the repo, add your module, and submit a PR.

For feature requests, bug reports, or collaboration ideas, open an issue.

--------------------------------------------------------------------------------
📢 Final Note
--------------------------------------------------------------------------------

SysCreep is a powerful tool for professionals and learners alike.  
Use it wisely. Stay ethical. Keep exploring.
