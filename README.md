#SEAN NOTES  
ALL COMMANDS AND PURPOSE
- whoami – Shows the current logged-in username.
- id – Displays user ID and group ID information.
- cd – Changes the current directory.
- ls – Lists files and directories in the current directory.
- touch – Creates a new empty file. Can also modify and update a file. If it exists, it will update the timestamp of the last modification.
- echo – Prints text or variables to the terminal. Shows the arguments you input (Anything you put after a command)
- cat – Displays the contents of a file.
- file – Shows the type of a file.
- cp – Copies files or directories.
- mv – Moves or renames files or directories.
- rm – Deletes files or directories.
Cool Computer Science Fact

- Modern CPUs use something called **speculative execution**.
- This means the computer **guesses** what your code will do next and starts doing it **before it's sure**.
- If it's right → the program runs faster!
- If it's wrong, it just throws away the work.

Why this matters:

- It helps programs run **super fast**.
- But it also caused some security problems in which the computer could accidentally look at things they shouldn't have or private files

I forgot to commit to the first Zoom meeting
Introduction to information technology
Study or use of systems for storing, retrieving, and sending information
All technology essentially just does these 3 things
All devices have packets, info, or data, as the best term
Apps were made to get a lot of data
They do something with this data
Someone takes a lot of plastic, and the machine builds something out of it

## 🧱 Hardware

**Hardware** refers to the **physical components** of a computer system that you can touch and see.

### Examples:
- CPU (Central Processing Unit)
- RAM (Random Access Memory)
- Hard drives / SSDs
- Monitor, Keyboard, Mouse
- Graphics card, Motherboard

> 🛠️ **Think of hardware as the "body" of the computer system.**

---

## 🧠 Software

**Software** refers to the **programs and operating systems** that run on the hardware and tell it what to do.

### Categories:
- **System software** (e.g., Windows, macOS, Linux)
- **Application software** (e.g., Google Chrome, Microsoft Word, games)

> 💡 **Software is like the "mind" that gives instructions to the hardware.**

---

## 🧬 Firmware

**Firmware** is a special type of software that is **permanently stored** in hardware devices.

- Typically found in ROM (Read-Only Memory)
- Controls low-level operations of hardware
- Runs before the operating system (e.g., BIOS or UEFI)

### Examples:
- BIOS on a PC
- Firmware on a router, printer, or smartphone

> ⚙️ **Firmware is the "built-in brain" of a hardware device.**

---

## 🧩 Kernel

The **Kernel** is the **core part of an operating system**.

- Acts as a **bridge between hardware and software**
- Manages system resources: CPU, memory, devices, etc.
- Controls low-level operations like process scheduling and device communication

### Types:
- **Monolithic kernels** (e.g., Linux)
- **Microkernels** (e.g., MINIX)
- **Hybrid kernels** (e.g., Windows NT)

> 🧠 **The kernel is like the "manager" of the computer's brain.**

---

## 📌 Summary

| Component | Description                              | Role                                           |
|----------|------------------------------------------|------------------------------------------------|
| Hardware | Physical parts of a computer             | Executes instructions from software            |
| Software | Programs that run on hardware            | Tells hardware what to do                      |
| Firmware | Permanent software in devices            | Controls device behavior at a low level        |
| Kernel   | Core of the operating system             | Manages communication between hardware & software |

Monolithic Kernel
When the Kernel and User space are in the same space
- Faster because there is no separation in memory between the user and kernel space
- If ANYTHING fails, the entire system fails
- If new services are added, the entire operating system needs to be modified
- We don't use this anymore
Microkernel
- Provides CPU scheduling
- Memory scheduling
- file management through system calls only
- If any service fails, it leads to system failure
- Anything new added, the whole system must be optimized
GUI
- Graphical User Interface
- essentially any graphics like logos, or the mouse
CLI
- Command Line Interface
