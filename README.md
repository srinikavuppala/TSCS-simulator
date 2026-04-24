**Thread Scheduling & Context Switching Simulator**
An interactive, browser-based visualization tool for OS thread scheduling algorithms. Designed for computer science students and educators to intuitively understand how CPUs manage threads, handle preemptive vs. non-preemptive scheduling, and process context switches.

**HTML5**
**JavaScript**
**Architecture** : Single File

🧩 Supported Algorithms
Round Robin (RR): Preemptive scheduling with a configurable time quantum.
First Come, First Served (FCFS): Non-preemptive execution strictly based on arrival order.
Shortest Job First (SJF): Non-preemptive execution prioritizing the shortest available burst time.
Priority Scheduling: Non-preemptive execution based on assigned priority levels (lower number = higher priority).

✨ Key Features
**Visualization & Animation**
Canvas-Rendered Gantt Chart: High-DPI aware timeline showing execution, idle periods, and context switches.
Play / Pause / Step Controls: Run the simulation automatically or advance it one time unit at a time.
Adjustable Speed: Scale the animation speed from 1x to 10x to match your learning pace.

**Deep OS Mechanics**
Live State Tracking: Watch threads transition dynamically between New → Ready → Running → Completed.
Ready Queue Monitor: Real-time view of which threads are queued and waiting for CPU time.
PCB Context Switch Inspector: View register-level details (PC, R0-R3, SP, FLAGS) being saved to and loaded from the Process Control Block during every switch.

**Performance Analytics**
Per-Thread Metrics: Instantly view Waiting Time, Turnaround Time, and Completion Time for every thread.
System Metrics: Track CPU Utilization %, Total Context Switches, and Total Elapsed Time.
Compare All Mode: Open a dashboard to view all 4 algorithms side-by-side, complete with mini Gantt charts and "Best" badges highlighting the most efficient algorithm.

🚀 Quick Start
No build tools, bundlers, or installations are required.

Download or clone this repository.
Open index.html in any modern web browser (Chrome, Firefox, Safari, Edge).
Optional: Run a local server for faster reloading:
python3 -m http.server 8000

🎮 How to Use
Add Threads: Enter an Arrival Time, Burst Time, and Priority (if applicable), then click Add Thread. Alternatively, click a Preset (Basic, Medium, or Complex) to auto-populate threads.
Select Algorithm: Click the desired algorithm tab in the header (Round Robin, FCFS, SJF, or Priority).
Configure: Adjust the Time Quantum slider (for Round Robin) and the Animation Speed slider.
Simulate: Click Play to watch the full simulation, or click Step to advance exactly one time unit at a time.
Inspect: When a context switch occurs, a detail panel automatically expands showing the exact register state being swapped.
Analyze: Once complete, view the metrics table below the chart, or click Compare All to see how other algorithms would have handled the same workload.

⌨️ Keyboard Shortcuts
Key                    Action
Space	            Play or Pause the simulation
→ (Right Arrow)	  Step forward one time unit
R	                Reset the simulation to the beginning

⚙️ Under the Hood
Zero Dependencies: The entire application is contained in a single index.html file (CSS in <style>, JS in <script>).
Styling: Tailwind CSS (via CDN) combined with custom CSS variables for a cohesive dark-mode UI.
Rendering: HTML5 Canvas handles the Gantt charts, dynamically scaling block widths and time-axis ticks based on simulation length.
Context Switch Overhead: Realistically modeled as a 1 time-unit penalty, visually represented as a dashed red block, and factored into all final time calculations.
