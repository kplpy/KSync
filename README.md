# KSync – Resumable File Transfer Tool

KSync is a Python-based desktop file transfer utility built with Tkinter.  
It is designed for reliable, interrupt-safe copying of files and folders with real-time progress tracking and resume capability.

---

## Features

- Resumable transfers using `.ksync` temporary files  
- Drag and drop support for files and folders  
- Session-based speed calculation for stable performance metrics  
- ETA estimation based on current session performance  
- Automatic disk space checking before and during transfer  
- Supports single files, multiple files, and entire folders  
- Overwrite or resume detection for existing files  
- Multi-threaded transfer (GUI remains responsive)  
- Live transfer logs stored locally  
- Automatic file append support for multi-item selection  
- Clean and simple Tkinter interface  

---

## How It Works

KSync copies data in chunks and writes them to a `.ksync` temporary file first.  
If the transfer is interrupted, it resumes from the last successfully written chunk instead of restarting.

Once completed, the temporary file is renamed to the final destination.

The application also supports drag-and-drop file selection and appending multiple files/folders into a single transfer session.

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
- Unstable environments (external interruptions)  
- Users needing resume capability without third-party tools  
- Multi-file transfer workflows using drag and drop  

---

## Notes

- Uses `.ksync` temporary files during transfer  
- Fully local tool (no internet dependency)  
- Designed for Windows environments (Tested on Windows Primarily)
