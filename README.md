<h1><p align="center" style="font-size:1.5rem;font-weight:normal"><img src="https://github.com/WebAssembly/web-assembly-logo/raw/master/dist/logo/web-assembly-logo-256px.png" alt="webassembly" /><br />Binaryen Installation via NPM</p></h1>

[![npm](https://img.shields.io/npm/v/@irongeek/binaryen?logo=npm)](https://www.npmjs.com/package/@irongeek/binaryen)
[![npm downloads](https://img.shields.io/npm/dt/@irongeek/binaryen?logo=npm)](https://www.npmjs.com/package/@irongeek/binaryen)
[![GitHub issues](https://img.shields.io/github/issues/IronGeek/binaryen?logo=github)](https://github.com/IronGeek/binaryen/issues)
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/IronGeek/binaryen?logo=github)](https://github.com/IronGeek/binaryen/releases)
[![License](https://img.shields.io/github/license/IronGeek/binaryen)](https://github.com/IronGeek/binaryen/blob/master/LICENSE)

This package will download, compile, and install the [WebAssembly](https://webassembly.org) Binaryen toolchain from https://github.com/WebAssembly/binaryen as [NPM](https://www.npmjs.com) global executables  

## Prerequisites

- [git](https://git-scm.com/)
- [cmake](https://cmake.org/)
- make 

## Installation

``` sh
npm install -g @irongeek/binaryen
```

> 📌 **NOTE**
> 
> Please give it some time to finish... 🙏
>
> Depends on your computer specs, the installation process might take a while, and because NPM suppresses all output from custom install script (_unless exception is thrown_), the process might seems like it's stuck or hanging while it's actually busy compiling the binaries.

## Included Tools

| Tools                      | Description |
| -------------------------- | ----------- |
| `wasm-opt`                 | Loads WebAssembly and runs Binaryen IR passes on it |
| `wasm-as`                  | Assembles WebAssembly in text format (currently S-Expression format) into binary format (going through Binaryen IR) |
| `wasm-dis`                 | Un-assembles WebAssembly in binary format into text format (going through Binaryen IR) |
| `wasm2js`                  | A WebAssembly-to-JS compiler. This is used by Emscripten to generate JavaScript as an alternative to WebAssembly |
| `wasm-reduce`              | A testcase reducer for WebAssembly files. Given a wasm file that is interesting for some reason (say, it crashes a specific VM), wasm-reduce can find a smaller wasm file that has the same property, which is often easier to debug. See the docs for more details |
| `wasm-shell`               | A shell that can load and interpret WebAssembly code. It can also run the spec test suite |
| `wasm-emscripten-finalize` | Takes a wasm binary produced by llvm+lld and performs emscripten-specific passes over it |
| `wasm-ctor-eval`           | A tool that can execute C++ global constructors ahead of time. Used by Emscripten |

## Known Issues

Must be run under bourne shell (`sh`) compatible terminal.

> _May or may not work on Windows using [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl)_.

## Acknowledgement

Mathias Buus for the original [webassembly-binary-toolkit](https://github.com/mafintosh/webassembly-binary-toolkit.git) installation script.

## License

This package is released under the terms of [The MIT License](https://github.com/IronGeek/binaryen/blob/master/LICENSE)
