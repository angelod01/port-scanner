# Basic Network Port Scanner

## Description
This project is a simple TCP port scanner designed to identify open ports on specified hosts. It supports scanning single IP addresses or domain names within a specified port range. The scanner uses multi-threading for faster scanning and provides verbose output for detailed scanning information. It also supports saving the scan results to a JSON file.

---

## Table of Contents
- [Features](#features)
- [Libraries](#libraries)
- [Getting Started](#getting-started)
  - [Requirements](#requirements)
  - [Installation](#installation)
- [Usage](#usage)
  - [Command Line Arguments](#command-line-arguments)
  - [Examples](#examples)

---

## Features
- Multi-threaded TCP port scanning for improved speed  
- Scans individual IP addresses or hostnames  
- Port range scanning with support for all ports (1-65535)  
- Input validation for target IP addresses
- Detect known vulnerabilities for specific servers (FTP, SSH, etc..)
- Verbose mode for detailed output  
- Save scan results to a JSON file  
- Color-coded output to easily identify open and closed ports  

---

## Libraries
- Standard libraries: `socket`, `threading`, `argparse`, `json`, `ipaddress`  
- External libraries: `tqdm` for progress bars, `termcolor` for colored terminal output, `IPython` for clearing output in Jupyter environments  

---

## Getting Started

### Requirements
- Python 3.7 or higher  
- Install required Python packages:

```bash
pip install -r requirements.txt
```

### Installation
```bash
git clone https://github.com/angelod01/port-scanner.git
```

```bash
cd port-scanner
```

## Usage
### Command Line Arguments
| Argument              | Description                                                               |
|-----------------------|---------------------------------------------------------------------------|
| `-t`, `--targets`     | Required. One or more IPs or domains to scan.                            |
| `-p`, `--port-range`  | Optional. Port range like `1-100` or `all` (default: `1-100`).            |
| `-T`, `--timeout`     | Optional. Timeout in seconds per scan attempt (default: `1.0`).          |
| `-n`, `--num-threads` | Optional. Number of concurrent threads (default: `10`).                  |
| `-o`, `--output`      | Optional. Save results to a file in JSON format.                         |
| `-v`, `--verbose`     | Optional. Verbose output during scan.                                    |

### Examples
Scan a single IP over default port range (1–100):
```bash
python main.py -t 192.168.1.1
```
Scan a domain over a custom port range:
```bash
python main.py -t example.com -p 20-80
```
Scan multiple targets:
```bash
python main.py -t 192.168.1.1 10.0.0.1 example.com
```
Scan all ports on a target with verbose output:
```bash
python main.py -t 192.168.1.1 -p all -v
```
Use 50 threads and set a longer timeout:
```bash
python main.py -t example.com -p 1-1024 -n 50 -T 3.0
```
Save scan results to a JSON file:
```bash
python main.py -t 10.0.0.1 -p 22-25 -o results.json
```

## Known Issues
- Service detection may fail if the server does not respond to banner grabbing.
- Some ports may appear closed due to firewalls or filtering mechanisms.
- Accuracy of vulnerability detection is limited to basic banner checks.

Use this tool responsibly and only on systems you have permission to scan.

## Disclaimer
This tool is intended for educational and authorized testing purposes only. Do not use it to scan or target systems you do not own or have explicit permission to test. Unauthorized scanning is illegal and unethical.





