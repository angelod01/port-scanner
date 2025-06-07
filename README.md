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
- [License](#license)

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


