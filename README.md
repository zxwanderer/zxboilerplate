# zxboilerplate
ZX Spectrum sjasmplus+vscode boilerplate

## How to use
1. Download and install Visual Studio Code: https://code.visualstudio.com/Download
2. Install Z80 Macro-Assembler extension: https://marketplace.visualstudio.com/items?itemName=mborik.z80-macroasm
3. Setup your enviropment in `.vscode/tasks.json`

That's all! Now you can use `Run build task` (Ctrl+Shift+B on Windows or ⌘+B on macOS by default) to compile your `main.asm` file.

## .vscode/tasks.json example:

```
{
    "version": "2.0.0",
    "tasks": [
        {
            "label": "build",
            "type": "shell",
            /*
            Available commands: 
            `make copy` copying builded snapshot to given directory/filename
            `make run`  run ZX Spectrum emulator with builded snapshot 
            */
            "command": "make copy",
            "options": {
                "cwd": "${workspaceFolder}",
                "env": {
                    // Custom project name. If not defined, directory name used.
                    "PROJECT_NAME": "project_name",
                    // ZX Spectrum emulator executable
                    "EMULATOR_BINARY": "xpeccy",
                    // Copying builded snapshot to this file
                    "COPY_SNAPSHOT_TO": "/tmp/quicksave.sna"
                }
            },
            "group": {
                "kind": "build",
                "isDefault": true
            },
            "isBackground": false,
            "presentation": {
                "echo": false,
                "reveal": "always",
                "focus": true,
                "panel": "shared",
                "showReuseMessage": false,
                "clear": true
            },
            "problemMatcher": "$errmatcher-sjasmplus"
        }
    ]
}
```
