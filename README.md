# Python-project_file-organizer
A Python-based file organizer that automatically categorizes and moves files into designated folders based on their types.  

---
## Overview

This script organizes files by:
- Scanning a target directory (`files/`)
- Detecting file types (documents, images, videos, etc.)
- Moving them into categorized folders automatically
- Dynamically creating new categories when encountering unknown file types  
- Logging all operations (including errors) for tracking and debugging

The program follows **modular design** (separated modules for sorting, configuration, and logging) and uses:
- **Metaprogramming (decorators)** for handling new file types dynamically
- **Regular Expressions** for file type detection
- **Error Handling & Logging** for robust performance

---
## Project Structure
```
Part2/
├── main.py
├── modules/
│ ├── init.py
│ ├── config.py
│ ├── file_sorter.py
│ └── logger.py
├── files/
└── logs.txt
```
---

## How to Use

1. **Clone the Repository**
   ```bash
   git clone https://github.com/flekke/part2.git
   cd part2
   ```
   
2. **Run the Script**
  ```bash
  python3 main.py
  ```
  The script will scan the files/ directory, organize files by type, and log all actions to logs.txt.

3. **Check Logs**
  All operations, including new categories and errors, are logged in logs.txt.

## Features
Modular structure for easy maintenance and extension

Dynamic handling of unknown file types via decorators

Regex-based categorization

Logging for debugging and tracking

## Limitations
Categorization relies solely on file extensions (files without or with non-standard extensions may not be sorted correctly).

Limited error handling (only PermissionError and generic exceptions are explicitly managed).

Logs are stored in a single file; may become large over time.



