# devspace

A lightweight Bash utility for automatically arranging and switching between desktop window layouts on Linux.

Built for the MATE desktop environment using the Marco window manager and X11.

## Features

- **Side-by-side layout:** Arranges Terminator on the left and Firefox on the right.
- **Stacked layout:** Arranges Terminator above Firefox.
- **Toggle mode:** Switches between side-by-side and stacked layouts.
- **Automatic window detection:** Finds existing Terminator and Firefox windows.
- **Automatic launching:** Starts missing applications when needed.
- **Dynamic Firefox geometry:** Reads window frame measurements instead of relying on hardcoded offsets.

## Requirements

devspace is designed for Linux systems running:

- **MATE Desktop** with the **Marco** window manager
- **X11** (not Wayland)
- **Bash**
- **Terminator**
- **Firefox ESR**

The following command-line utilities are also required:

- `wmctrl`
- `xdotool`
- `xprop`

On Debian-based distributions, including Parrot OS, install the required packages with:

```bash
sudo apt install terminator firefox-esr wmctrl xdotool x11-utils
```

## Installation

Clone the repository:

```bash
git clone https://github.com/TinCanTed/devspace.git
```

Enter the project directory:

```bash
cd devspace
```

Make the script executable:

```bash
chmod +x devspace
```

Run it:

```bash
./devspace
```

## Usage

### Side-by-side layout

```bash
./devspace
```

Arranges Terminator on the left half of the screen and Firefox on the right half.

### Stacked layout

```bash
./devspace stacked
```

Arranges Terminator in the top half of the screen and Firefox in the bottom half.

### Toggle between layouts

```bash
./devspace toggle
```

Switches between the side-by-side and stacked layouts.

## Run from Anywhere (Optional)

To run `devspace` without typing `./`, copy it into your personal executable directory:

```bash
mkdir -p ~/.local/bin
cp devspace ~/.local/bin/devspace
chmod +x ~/.local/bin/devspace
```

If `~/.local/bin` is included in your `PATH`, you can now run:

```bash
devspace
devspace stacked
devspace toggle
```

This allows you to switch layouts without navigating to the project directory.
