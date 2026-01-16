🎸 FPGA Guitar Synthesizer with Karplus–Strong & VGA Visualization

This repository documents an FPGA-based digital guitar synthesizer implemented as a hardware design project.
Due to course and academic integrity policies, the source code is not publicly shared.
Instead, this repository contains the final presentation, system architecture, and lab demonstration images.

📌 Project Overview

This project implements a real-time digital guitar on an FPGA using physical modeling synthesis and synchronized visual feedback.

The system:

Generates realistic plucked-string audio using the Karplus–Strong algorithm

Displays a guitar with 6 animated vibrating strings via VGA

Accepts real-time user input through a PS/2 keyboard

Synchronizes audio output and VGA animation on hardware

All components run entirely on the FPGA in real time.

🧠 System Architecture

The design is fully modular and hardware-driven.

Key Subsystems

PS/2 Input System

Reads keyboard scancodes

Keys 1–6 select guitar strings

Spacebar triggers a pluck

Ensures only one string plays at a time

Karplus–Strong Audio Core

Physical modeling synthesis using:

Circular delay-line buffer

Noise burst (pluck)

Averaging low-pass filter

Produces realistic decaying string vibration

Audio Output System

Real-time audio mixing

FPGA audio controller + DAC interface

Synchronized playback with visuals

VGA Visualization

640×480 static guitar background (MIF image)

Animated string vibration per pluck

Animation decays naturally with sound

A full block diagram and FSM breakdown are included in the presentation.

🎮 User Interaction
Input	Function
1 – 6	Select guitar string
Spacebar	Pluck selected string
VGA Output	Visual vibration animation
Speakers	Real-time synthesized audio
🖼️ Project Media

This repository includes:

📑 Final Presentation (PDF) – full system explanation, diagrams, FSMs, and design decisions

📸 Lab Photos – real FPGA demo with VGA output and audio playback

See the uploaded presentation for detailed block diagrams, FSMs, and timing explanations.

🧩 Engineering Challenges Solved

Prevented unintended retriggering when switching strings mid-decay

Tuned string frequencies through empirical testing for realistic tone

Achieved human-visible vibration speeds on VGA via timing control

Precisely positioned strings on a complex background image

Debugged and verified timing across audio + VGA pipelines

🚀 Future Extensions

Dynamic pitch control across a full virtual fretboard

PS/2 mouse scroll wheel for:

Pluck intensity

Volume control

Polyphonic playback (multiple strings simultaneously)

MIDI input support
