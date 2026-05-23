# KSync – Resumable File Transfer Tool

KSync is a Python-based desktop file transfer utility built using Tkinter and TkinterDnD2.
It is designed for reliable, interruption-safe file and folder transfers with resume capability, integrity verification, real-time metrics, and responsive GUI performance.

---

## Features

* Resumable transfers using `.ksync` temporary files
* SHA256 file verification after transfer completion
* Drag and drop support for files and folders
* Pause, resume, and cancel transfer controls
* Real-time transfer speed calculation
* Estimated remaining time (ETA) tracking
* Session-based performance metrics
* Automatic disk space checking before and during transfer
* Supports single files, multiple files, and entire folders
* Resume or overwrite detection for existing files
* Multi-threaded transfer engine (GUI remains responsive)
* Live progress bar with percentage tracking
* Real-time transferred and remaining size display
* Automatic append support for multi-item selection
* Transfer logging system with timestamped logs
* Menu bar controls for transfer management and logs
* Always-on-top mode support
* Windows executable packaging support using PyInstaller
* Clean and lightweight desktop interface

---

## How It Works

KSync transfers files in chunks and writes them to a temporary `.ksync` file first.
If the transfer is interrupted, the application resumes from the last successfully written byte instead of restarting the entire transfer.

When transfer completion is reached:

1. The temporary `.ksync` file is renamed to the final destination file
2. Optional SHA256 verification compares source and destination integrity
3. Transfer logs are saved locally for tracking and debugging

The application also supports drag-and-drop file selection and multi-item transfer sessions.

---

## Transfer Safety

KSync includes several mechanisms to improve transfer reliability:

* Resume support for interrupted transfers
* Corrupted temporary file detection
* Storage availability checking during transfer
* SHA256 integrity verification
* Safe overwrite handling
* GUI-safe threaded operations
* Automatic temporary file cleanup logic

---

## Key Design Goals

* Prevent data loss during interruptions
* Maintain accurate session-based transfer metrics
* Provide transfer integrity verification
* Keep the interface simple and lightweight
* Maintain responsive GUI performance during large transfers
* Support practical Windows desktop workflows

---

## Use Cases

Ideal for:

* Large file transfers
* External drive transfers
* Interrupted or unstable transfer environments
* Multi-file drag-and-drop workflows
* Users needing resume support without third-party utilities
* Long-running file operations requiring integrity verification

---

## Technologies Used

* Python
* Tkinter
* TkinterDnD2
* Threading
* hashlib (SHA256 verification)
* shutil
* PyInstaller

---

## Notes

* Uses `.ksync` temporary files during transfer
* Fully local application (no internet dependency)
* Designed primarily for Windows environments
* Tested mainly on Windows systems
* SHA256 verification can be enabled or disabled from the Options menu

---

## Build Command (PyInstaller)

```bash
pyinstaller --onefile --windowed --icon=ico/KSync.ico --add-data "ico;ico" --collect-all tkinterdnd2 transfer.py
```
