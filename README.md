# Conway's Game of Life

A fully functional implementation of **Conway's Game of Life**, built from the ground up using my custom **LiteEngine** game engine.

![Conway's Game of Life](/media/CGoL.gif)

Conway's Game of Life is a cellular automaton where simple rules governing neighboring cells produce surprisingly complex behavior. This project serves as both a playable implementation of the simulation and an example of what LiteEngine is capable of.

## Features

* Fully functional Conway's Game of Life simulation
* Interactive cell placement
* Pause and resume simulation
* Real-time engine overlay with FPS display
* Built using my custom **LiteEngine** engine
* Lightweight and designed to run on modest hardware

---

## Controls

| Key / Input           | Action                    |
| --------------------- | ------------------------- |
| **Space**             | Toggle pause / resume     |
| **F3**                | Toggle the engine overlay |
| **Left Mouse Button** | Toggle a cell's state     |
| **Escape**            | Exit the game             |

> **Note:** The engine overlay currently displays FPS information.

---

## How to Play

The simulation starts **unpaused**.

If you want to create your own starting configuration:

1. Press **Space** to pause the simulation.
2. Use the **Left Mouse Button** to activate or deactivate cells.
3. Arrange the board however you like.
4. Press **Space** again to resume the simulation.
5. Watch your creation evolve according to Conway's rules.

You can experiment with anything from simple patterns to large, chaotic configurations.

---

## Building

### Windows Only

A pre-built `.exe` is included in the `build` directory. On some Windows 11 systems, it may run without any additional setup. However, depending on your system configuration, you may need to build the project yourself.

### Requirements

Before building, you will need:

* Windows
* MinGW (or another supported C++ compiler)
* GLFW
* FreeType
* Git

### Build Instructions

#### 1. Clone the repository

Clone the repository to your local machine:

```bash
git clone <repository-url>
cd <repository-directory>
```

#### 2. Configure dependencies

The project currently uses **absolute paths** for GLFW and FreeType.

Open the project's configuration files and update the GLFW and FreeType paths so that they point to the appropriate locations on your system.

#### 3. Configure the compiler

Open `config.bat`.

If you are using MinGW, verify that it is installed and available through your system's PATH:

```bash
mingw --version
```

If you are using a different compiler, modify `config.bat` accordingly.

#### 4. Build the project

Run the following batch files in order:

```text
clean.bat
config.bat
build.bat
```

Check the output for any errors.

If the build completes successfully, you can either run:

```text
run.bat
```

or navigate to the `build` directory and launch the generated `.exe` directly.

---

## About LiteEngine

This project was built as an example application for **LiteEngine**, my custom game engine written in C++.

LiteEngine is designed with performance and simplicity in mind, with a focus on data-oriented architecture and efficient handling of large numbers of entities. Conway's Game of Life provides a useful test case for the engine because the simulation can involve large numbers of cells being updated every frame.

More projects and examples will be added as LiteEngine continues to develop.

---

## Conway's Game of Life

The simulation follows the classic rules:

1. A living cell with fewer than two living neighbors dies from underpopulation.
2. A living cell with two or three living neighbors survives.
3. A living cell with more than three living neighbors dies from overpopulation.
4. A dead cell with exactly three living neighbors becomes alive.

Despite these simple rules, the system can produce stable structures, oscillators, spaceships, and highly complex emergent behavior.

---

## License

*GNU General Public License v3.0*
