# KSync – Resumable File Transfer Tool

KSync is a Python-based desktop file transfer utility built with Tkinter.  
It is designed for reliable, interrupt-safe copying of files and folders with real-time progress tracking and resume capability.

---

## Features

- Resumable transfers using `.ksync` temporary files  
- Session-based speed calculation for stable performance metrics  
- ETA estimation based on current session performance  
- Automatic disk space checking before and during transfer  
- Supports single files and entire folders  
- Overwrite or resume detection for existing files  
- Multi-threaded transfer (GUI remains responsive)  
- Live transfer logs stored locally  
- Clean and simple Tkinter interface  

---

## How It Works

KSync copies data in chunks and writes them to a `.ksync` temporary file first.  
If the transfer is interrupted, it resumes from the last successfully written chunk instead of restarting.

Once completed, the temporary file is renamed to the final destination.

---

## Key Design Goals

- Prevent data loss during interruption  
- Maintain accurate session-based performance stats  
- Keep tool lightweight and dependency-free  
- Provide simple but functional UI for file management  

---

## Use Case

Ideal for:

- Large file transfers  
- Unstable environments (USB removal risk, interruptions)  
- Users needing resume capability without third-party tools  

---

## Notes

- Uses `.ksync` temporary files during transfer  
- Fully local tool (no internet dependency)  
- Designed for Windows environments
