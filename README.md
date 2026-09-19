# 8 Bit Racer

**8 Bit Racer** is a top-down racing game built in Python using Pygame.

I originally created the project independently as my A-Level Computer Science programming project. It took roughly **six months** to build and became a genuine passion project rather than just coursework. The final project received **66/70 marks**.

At the time, I was largely self-taught in Python and used the project to explore areas such as game development, persistent data, user authentication, AI behaviour, custom development tools and larger multi-file program design.

## Features

The original project includes:

* Player accounts with hashed passwords
* JSON-based user data and saved records
* Multiple dynamically loaded tracks
* Three-lap racing with checkpoints
* AI-controlled opponents
* Sound effects and music
* Player settings
* Track records
* A custom track-building tool
* AI waypoint generation for custom tracks

Tracks are represented as **64 × 36 tile grids** stored in JSON, allowing the game to load different circuits without hard-coding each one.

One of the main strengths of the project was its scope. Rather than building only a single race, I attempted to build a reusable game system with persistent users, configurable tracks, AI racers and tools for creating additional content.

As an early self-taught project, it also has limitations. Some systems are more tightly coupled than I would design them today, error handling is relatively basic, and parts of the architecture developed organically as the project grew. The original version was also heavily designed around Windows.

## AI-Assisted Recovery

Several months after completing the project, I moved the surviving codebase to a new computer and discovered that the entire original `assets` and `data` directories had been lost.

The Python source code and approximately **342 pages of original development documentation** survived.

In 2026, I used OpenAI's ChatGPT to help reconstruct the missing runtime files by analysing my original source code and documentation.

AI assistance was used to:

* Recreate replacement graphics and audio
* Reconstruct the expected JSON data structures
* Create replacement playable tracks
* Restore the user-data structure
* Make file paths work across Windows and macOS
* Add fallbacks for missing fonts and unavailable audio
* Remove an unnecessary NumPy dependency
* Fix an edge case in the original track-builder AI waypoint generation
* Add basic verification and launch scripts

The replacement assets and track layouts are **not the original files from my submitted project**.

The game's original concept, design, architecture, systems and source code were created by me. AI was introduced only after completion to recover lost files and make the surviving project runnable again.

**This README itself was also written with AI assistance.**

## Running the Project

Python 3 and Pygame are required.

### Windows

Open Command Prompt or PowerShell inside the project folder:

```bash
python -m venv .venv
.venv\Scripts\activate
python -m pip install -r requirements.txt
python run_game.py
```

### macOS

Open Terminal inside the project folder:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python run_game.py
```

You can optionally verify the reconstructed files first with:

```bash
python verify_recovery.py
```

### Demo Account

```text
Username: demo
Password: Password1
```

New accounts can also be created through the game.

## Final Note

I have kept this repository primarily as a record of one of my first substantial programming projects.

There are many things I would structure differently with the experience I have now, but the project represents an important stage in learning how to take a large idea, break it into systems, solve problems independently and turn it into a working piece of software.
