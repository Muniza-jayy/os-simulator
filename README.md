# My OS Simulator

A C++ based operating system simulator that demonstrates key OS concepts:
- **Process Scheduling**: First-Come First-Serve (FCFS), Priority, and Round-Robin
- **Resource Management**: dynamic allocation of RAM, Disk, and CPU cores
- **Mode Switching**: User and Kernel modes with safe critical-section handling
- **Simulated File System**: create and delete files to observe disk usage
- **Mini-Applications**: Notepad, Calculator, Clock, File Manager, Minesweeper, Music Player, Calendar, Timer, Terminal, File Explorer, System Monitor

---

## Features

- **Multitasking & Scheduling**  
  - FCFS  
  - Priority-based (numeric priorities)  
  - Round-Robin (configurable time quantum)

- **Resource Management**  
  - Track and allocate RAM & Disk per process  
  - Allocate CPU cores to running processes  

- **Process Lifecycle**  
  - Create, terminate, block (minimize), resume  
  - Ready/Running/Blocked states

- **File System Simulation**  
  - Create and delete files in a `simulated_disk/` directory  
  - Maintain an in-memory map of filenames to sizes

- **Interactive CLI**  
  - Menu-driven interface  
  - Signal handling (Ctrl+C for graceful shutdown)

---

## Getting Started

### Prerequisites

- A C++17–compatible compiler (e.g., `g++`, `clang++`)
- POSIX threads (`-pthread`)
- CMake (optional) or a simple Makefile

### Clone the Repository

```bash
git clone https://github.com/Muniza-jayy/my-os-simulator.git
cd my-os-simulator
```

### Build

#### With CMake (recommended)

```bash
mkdir build && cd build
cmake ..
make
```

#### Manual Compile

```bash
g++ -std=c++17 -pthread -o os_simulator \
    src/*.cpp
```

---

## Usage

```bash
./os_simulator [RAM_MB] [DISK_MB] [CORES]
```

- `RAM_MB` &mdash; Total system RAM in megabytes (default: 2048)  
- `DISK_MB` &mdash; Total disk space in megabytes (default: 102400)  
- `CORES` &mdash; Number of CPU cores (default: 4)

Once started, use the interactive menu to:
1. Launch mini-apps with resource requirements  
2. Display system and resource status  
3. Create/delete files in the simulated file system  
4. Block, resume, or terminate processes  
5. Toggle modes, save/load playlists, and more  
6. Gracefully shut down the simulator

---

## Contributing

Contributions are welcome! Feel free to:
- Open issues for bugs or feature requests  
- Submit pull requests with improvements or new mini-apps  

Please follow standard GitHub workflow and code style conventions.

---

## License

This project is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

---

© 2025 Muniza-jayy
