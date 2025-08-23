#SEAN NOTES  
HOMEWORK:
- Explain the top-level directories in the Linux file system
-  Root  
The top-level directory. Everything starts from here.

bin  
Essential command-line programs used by everyone (ls, cp, mv).

boot  
Files required to start the system, including the kernel.

dev  
Device files representing hardware like hard drives, USBs, etc.

etc  
Configuration files for the system and installed applications.

home  
Personal directories for users. For example, home/alex for user alex.

lib  
Shared libraries needed by system programs in bin and sbin.

media  
Mount point for automatically attached external devices (USB, CD).

mnt  
Mount point for manually attached drives or file systems.

opt  
Location for optional or third-party software packages.

proc  
Virtual directory containing information about system processes and kernel state.

root  
Home directory for the root (administrator) user.

run  
Temporary directory holding information about running services and sessions.

sbin  
System binaries used by the administrator (shutdown, mount, etc.).

srv  
Data for services provided by the system (web server, FTP, etc.).

sys  
Virtual directory exposing hardware and device information.

tmp  
Temporary files used by applications and cleaned at reboot.

usr  
Installed software and user utilities that remain constant (games, tools).

The system is organized by purpose.

Files that don’t change often (like programs and libraries) are kept separate from files that change a lot (like logs and settings).

This makes it easier to back up or protect important parts of the system.

Different parts of the system can be stored on different drives.

For example, your files in /home can be on one drive, and system files in /usr on another.

This helps manage space better and improves speed or security.

It makes sure the computer can start up properly.

Basic commands and tools are stored in places like /bin and /sbin, which are always available during boot.

Other stuff like user programs can load later.

Helps keep the system safe and running well.

If a user fills up their space in /home, it won’t break the whole system.

Same with log files in /var or temp files in /tmp.

Better security and control.

Important system files are stored in folders that only the admin (root) can change.

This prevents mistakes and hacking.

Everything follows a standard layout.

The directory structure is the same across most Linux systems.

That makes it easier for people and programs to know where things are.

It comes from older Unix systems.

Back then, they split things up because of small disk sizes.

Today, the structure still helps keep Linux flexible and reliable.






var  
Variable data files like logs, mail, and print queues.
ALL COMMANDS AND PURPOSE
- whoami – Shows the current logged-in username.
- id – Displays user ID and group ID information.
-    When a user is created in Linux or Unix, they get a User ID and Group ID. They both tend to have your name in them, and if you are in any other groups, you will be given those group IDs as well
- cd – Changes the current directory.
- ls – Lists files and directories in the current directory.
- touch – Creates a new empty file. Can also modify and update a file. If it exists, it will update the timestamp of the last modification.
- echo – Prints text or variables to the terminal. Shows the arguments you input (Anything you put after a command)
- cat – Displays the contents of a file.
- file – Shows the type of a file.
- cp – Copies files or directories.
-  Same Syntax as mv
- mv – Moves or renames files or directories.
-  mv SOURCE DESTINATION
-  SOURCE  = The path to a file
-  DESTINATION = Where you want to put the file
-   EX: mv(/home/sean/file2.txt) (/etc/crazy)
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

The **terminal** is a program where you type commands to talk to your computer.
- The **console** is the screen or place where the terminal shows what you type and the computer's response.
- The **shell** is the part that understands your commands and tells the computer what to do.
- There are different kinds of shells, like bash and zsh.
- The terminal is the window, the console is what you see in it, and the shell is like the brain that runs the commands.

File Systems
- Why it's important:
- Helps the computer find and open your files.
- Lets you organize stuff into folders.
- Keeps track of used and empty space.
- Makes sure files are saved and opened the right way.

---

Types of File Systems (and What They Do)

FAT32
- Works on most computers (Windows, Mac, Linux).
- Good for USB drives and SD cards.
- Can't hold files bigger than 4GB.
- Simple, but not super secure.

NTFS
- Used by Windows computers.
- Can hold very large files.
- Has extra features like file protection and encryption.
- Mac can read it, but can't always write to it.

exFAT
- Works on Windows and Mac.
- Great for big files and external drives.
- Doesn’t have extra features like NTFS.

ext4
- Used mostly by Linux.
- Fast and good for large storage.
- Windows doesn’t support it by default.

Understanding the Linux File System
- Like a file cabinet
-  Organized in a simple manner
-    A bunch of folders or "Directories"
-     There is a "Root folder" or just the "Root", and it is depicted as a slash
-  This folder is basically the start of all the files
-  You can enter the root directory and use it to enter other directories
-  The user starts outside of the file system. You can use the pwd command to find where you are in the file system
- *Root*
-  Pwd = /
- *Bin*
-  Pwd = /Bin
- *Home*
-  Pwd = /home
-   Sean
-    (File)file2.txt
-   Khalid
-    Random
-     (File)file7.txt
-   Christian
-   Pwd = home/Sean
- *Var*
-  Logs
-   (File)Messages
-  Pwd = /Var
- *Etc*
-  Crazy
-   (File)file6.txt
-  ssh
-   sshd
-    (File)sshd_config
-  Pwd = /Etc
- cd (Change) Directory
-  You need to specify where to start and what route to take
-  Let's say I want to go to my directory from root
- Rules
-  All files and directories are separated by a "/"
-  Absolute path: You must start from the root directory
-  The Pwd won't say that you are in a file
-  Additional info
-  / = Root directory
-  Root = SUPER user (admin)
-  /root root user's home directory
-  Pwd = Personal Working DIRECTORY
There are 2 paths
 Absolute Path
 Starts from root and has a / between each location (Very simple)
Relative Path
- .=Current working directory
-  The dot represents where we are
-  We can use it in place of where we currently are if we want to move a file or folder
-  ..= parent diriectory
-   Has Child directories
-     It works as simply as it sounds
Each command has a default function
- options lets you change that
HOMEWORK
Look through history and try to get CHATGPT to format a nice format in md format basicall copy and past what we did today from history
research API methods and what it is, then take your answer and put it into our website formatted nicely
