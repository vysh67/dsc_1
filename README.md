📡 Simulation of a Simple Network Protocol using Finite State Machine (FSM)
📌 Overview

This project demonstrates the use of Finite State Machines (FSMs), a Theory of Computation (TOC) concept, to simulate a simple network communication protocol.
The simulation models a communication process with four states: Idle, Connecting, Transmitting, and Disconnected, showing how devices interact in a state-driven manner.

The project is implemented in Python and tested with different event sequences to verify correct behavior.

🚀 Features

Models four fundamental states of a network protocol:

Idle

Connecting

Transmitting

Disconnected

Event-driven state transitions (connect_request, ack_received, send_data, disconnect, timeout)

Simulates a client-server style interaction

Demonstrates TOC application in computer networks

🛠️ Tech Stack

Language: Python

Concepts: Finite State Machine (FSM), Theory of Computation (TOC)

⚙️ Setup & Execution
1️⃣ Prerequisites

Install Python 3.10+

2️⃣ Steps to Run

Clone or download this repository.

git clone https://github.com/vysh67/TOC-FSM-Network-Simulation.git
cd TOC-FSM-Network-Simulation


Open the project folder in VS Code or any editor.

Run the Python file:

python fsm_network_simulation.py

📖 Example Simulation
Python Code Snippet
fsm = NetworkProtocolFSM()

fsm.on_event('connect_request')  # Idle → Connecting
fsm.on_event('ack_received')     # Connecting → Transmitting
fsm.on_event('send_data')        # Data sent, remain Transmitting
fsm.on_event('disconnect')       # Transmitting → Disconnected
fsm.on_event('connect_request')  # Disconnected → Connecting
fsm.on_event('timeout')          # Connecting → Disconnected

Sample Output
Current State: Idle | Event: connect_request
New State: Connecting

Current State: Connecting | Event: ack_received
New State: Transmitting

Data sent.
Current State: Transmitting | Event: disconnect
New State: Disconnected

🎯 Learning Outcomes

FSMs provide a structured way to model network protocols.

Demonstrated TOC principles applied to real-world systems.

Gained insights into protocol design, error handling, and verification.