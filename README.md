**Thread Scheduling & Context Switching Simulator**
An interactive, browser-based visualization tool for OS thread scheduling algorithms. Watch threads transition through states, observe context switches at the register level, and compare scheduling strategies in real time.

HTML5
JavaScript 
Architecture : Single File

✨ Features
4 Algorithms: Round Robin (configurable quantum), FCFS, SJF, and Priority scheduling
Animated Gantt Chart: Canvas-rendered timeline with color-coded execution, idle, and context switch blocks
Live State Tracking: Real-time New → Ready → Running → Completed state indicators
Context Switch Inspector: View simulated PCB save/load operations (PC, Registers, SP, Flags)
Performance Metrics: Waiting time, turnaround time, CPU utilization, and context switch overhead
Compare All Mode: Side-by-side Gantt charts and metrics for every algorithm simultaneously
🚀 Getting Started
No build step required. Simply open index.html in any modern web browser.

# Or serve it locally:git clone https://github.com/srinikavuppala/thread-scheduling-simulator.gitcd thread-scheduling-simulatorpython3 -m http.server 8000
🎮 How to Use
Add Threads via the sidebar or load a preset (Basic, Medium, Complex)
Select an Algorithm (Round Robin, FCFS, SJF, Priority) from the top tabs
Adjust Settings like Time Quantum and Animation Speed
Hit Play (or Space) to watch the simulation, or use Step (→) to advance manually
View Metrics once the simulation completes
Click Compare All to analyze all algorithms at once
⌨️ Keyboard Shortcuts
 Key          Action
Space	    Play / Pause
→	        Step forward
R	        Reset simulation

🛠️ Technical Details
Zero Dependencies: Single self-contained HTML file (Tailwind CSS & Font Awesome loaded via CDN)
Rendering: HTML5 Canvas (Retina/HiDPI aware)
Context Switch Overhead: Fixed at 1 time unit per switch, factored into all metrics
📄 License
This project is licensed under the MIT License.
