# Sprite VS Code Extension

Browse and edit files on [Sprites.dev](https://sprites.dev) sandboxes directly from VS Code.

## What it does

This extension provides a **FileSystemProvider** that lets you work with files on remote Sprites as if they were local:

- Browse Sprite filesystems in VS Code's explorer
- Open, edit, and save files directly on the Sprite
- Create, rename, and delete files/folders
- Open interactive terminal sessions with full TTY support
- Create and manage Sprites from VS Code

## How it works

The extension uses the official `@fly/sprites` SDK to communicate with Sprites.dev. Files are read/written via shell commands (`cat`, `base64`, `stat`, `ls`, etc.) tunneled through the SDK's exec API over HTTPS.

URI format: `sprite://sprite-name/path/to/file`

## Setup

1. Install the extension
2. Run `Sprite: Set API Token` and enter your Sprites.dev API token
3. Run `Sprite: Open Sprite` to add a Sprite as a workspace folder

## Commands

| Command | Description |
|---------|-------------|
| `Sprite: Set API Token` | Configure your Sprites.dev API token |
| `Sprite: Open Sprite` | Open a Sprite as a workspace folder |
| `Sprite: Create Sprite` | Create a new Sprite |
| `Sprite: Open Terminal` | Open an interactive shell on a Sprite |
| `Sprite: Delete Sprite` | Delete a Sprite |
| `Sprite: Refresh Files` | Refresh the file explorer |

## Usage

1. Press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows/Linux)
2. Run `Sprite: Open Sprite`
3. Select a Sprite and path to open
4. The Sprite's filesystem appears in VS Code's explorer
5. Edit files as normal - changes save directly to the Sprite

## Requirements

- VS Code 1.85.0+
- Sprites.dev API token
- Node.js 24+ (for the SDK)

## License

MIT
