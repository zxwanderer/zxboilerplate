# zxboilerplate
ZX Spectrum sjasmplus+vscode boilerplate

## How to use
1. Download and install Visual Studio Code: https://code.visualstudio.com/Download
2. Install Z80 Macro-Assembler extension: https://marketplace.visualstudio.com/items?itemName=mborik.z80-macroasm
3. Install ZX Spectrum emulator [sjasmplus](https://github.com/z00m128/sjasmplus) (Windows) or [Xpeccy](https://github.com/samstyle/Xpeccy) (Linux)
4. Install `make` utilite (Windows).
5. Setup your enviropment in `.vscode/tasks.json`. See comments in this file.

That's all! Now you can use `Run build task` (Ctrl+Shift+B on Windows or ⌘+B on macOS by default) to compile your `main.asm` file.

## Available commands:
`make build` Default: build project
`make run`  Build and run snapshot in emulator
`make copy` Build and copy snapshot to given path
`make clean` Remove artifacts
