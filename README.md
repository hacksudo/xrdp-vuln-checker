
# 🛡️ XRDP Vulnerability Checker

### A safe, non-exploit Bash tool to detect XRDP security risks and CVE-affected versions.

---

## 📘 Overview

The **XRDP Vulnerability Checker** is a lightweight and safe Bash script designed for:

* Security auditors
* Penetration testers
* System administrators
* Linux hardening teams

The script performs **PASSIVE detection only** and analyzes:

* XRDP installation status
* XRDP service state
* XRDP version and CVEs
* Public port exposure (0.0.0.0:3389)
* Weak XRDP configuration settings
* Color-coded vulnerability reporting

This tool is **100% safe** — it **does not exploit** anything or modify system files.

---

## ✨ Features

| Feature                        | Description                            |
| ------------------------------ | -------------------------------------- |
| 🔎 XRDP installation detection | Checks if package & binaries exist     |
| 🔎 XRDP version scan           | Detects version for CVE mapping        |
| 🧨 CVE detection               | Flags vulnerable versions              |
| 🌐 Port exposure check         | Determines if XRDP is publicly exposed |
| ⚙️ Config audit                | Highlights weak settings               |
| 🎨 Color-coded output          | Red = vulnerable, Green = safe         |
| 💼 VAPT-ready                  | Safe for enterprise testing            |

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/yourname/xrdp-vuln-checker.git
cd xrdp-vuln-checker
```

---

## ▶️ Usage

Give the script execution permission:

```bash
chmod +x xrdp_check.sh
```

Run the scanner:

```bash
./xrdp_check.sh
```

---

## 🧪 Example Output

```
========================================
        XRDP Vulnerability Check
========================================

[*] Checking if XRDP is installed...
[ INSTALLED ] XRDP Version: 0.9.17

[*] Checking XRDP service status...
[ RUNNING ] XRDP service is active

[*] Checking if XRDP port 3389 is exposed...
[ VULNERABLE ] XRDP is listening on 0.0.0.0:3389 (internet exposed)

[*] Checking for known XRDP vulnerabilities...
[ VULNERABLE ] XRDP version < 0.9.17
Associated CVEs:
 - CVE-2022-23613
 - CVE-2022-23614
 - CVE-2021-4011

[*] Checking XRDP configuration...
[ WEAK ] XRDP allows all channels (clipboard/file copy risk)
[ HIGH-BPP ] 32-bit color depth enabled (possible DOS attack surface)

========================================
              SCAN COMPLETE
========================================
```

## 🧩 CVE Reference Table

### 🔥 XRDP Vulnerabilities Covered

| CVE                | Description                   | Affected Versions |
| ------------------ | ----------------------------- | ----------------- |
| **CVE-2022-23613** | Use-after-free → RCE          | < 0.9.17          |
| **CVE-2022-23614** | XRDP auth bypass              | < 0.9.17          |
| **CVE-2021-4011**  | Heap overflow                 | Multiple          |
| **CVE-2018-19961** | DoS via malformed data        | Older XRDP        |
| **CVE-2018-19965** | Info disclosure via clipboard | Multiple          |

---

## 📂 Project Structure

```
xrdp-vuln-checker/
│
├── xrdp_check.sh          # Main scanning script
└── README.md              # Documentation
```

---

## 🤝 Contributing

Contributions are welcome!

You may add:

* More CVEs
* Additional config checks
* JSON / HTML reporting
* Custom flags & parameters

---

## 📜 License

This project is licensed under the **MIT License**.

---

## ⚠️ Disclaimer

This tool performs **only SAFE vulnerability detection**.
It does **NOT** perform exploits or unauthorized access.
Use only on systems you own or have explicit permission to assess.

---

## ⭐ Support the Project

If this helped you, please give the repo a ⭐ on GitHub!

---
