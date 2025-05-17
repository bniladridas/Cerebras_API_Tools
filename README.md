
# Cerebras API Tools

**Intelligence, unleashed.**  
Build fast. Create smart.  

Qwen3-32B on Cerebras Inference powers instant reasoning at 2,400 tokens per second. With hybrid reasoning, agentic support, and advanced tool calling, it outshines GPT-4.1 and Claude Sonnet 3.7—open-weight and ready for production.

## What You Get

- **Cerebras CLI**: A sleek command-line tool for instant chat completions.  
- **Cerebras Web UI**: An intuitive interface for seamless model interaction.  

## Start in Minutes

Clone, configure, and build with ease.

```bash
git clone https://github.com/bniladridas/Cerebras_API_Tools.git
cd cerebras_infra

# Set your API key
echo "CEREBRAS_API_KEY=your_api_key_here" > .env

# Build
mkdir build
cd build
cmake ..
make
```

### Run CLI
```bash
./cerebras_cli --model qwen-3-32b --prompt "You are a helpful assistant."
```

### Run Web UI
```bash
./cerebras_server
# Visit http://localhost:8080
```

## Requirements

- CMake 3.10+  
- C++17-compatible compiler  
- libcurl, nlohmann/json libraries  

### Install Dependencies

**macOS**  
```bash
brew install cmake curl nlohmann-json
```

**Ubuntu/Debian**  
```bash
sudo apt update
sudo apt install cmake libcurl4-openssl-dev nlohmann-json3-dev
```

## Build

```bash
mkdir build
cd build
cmake ..
make
```

Update after changes:  
```bash
cd build
cmake ..
make
```

## Use

### CLI
```bash
./cerebras_cli --model qwen-3-32b --prompt "You are a helpful assistant."
```

**Options**:  
- `--model`: Select model (default: qwen-3-32b)  
- `--prompt`: Set system prompt  
- `--help`: View all options  

**Recommended Prompt**:  
```
You are a CLI assistant powered by Qwen3 on Cerebras. Deliver concise, machine-readable output, optimize for speed, and follow best practices.
```

### Web UI
```bash
./cerebras_server --port 8080
```

Visit `http://localhost:8080` to:  
- Choose models  
- Set prompts  
- Chat interactively  
- View history  

**Options**:  
- `--port`: Set port (default: 8080)  
- `--help`: View all options  

## Setup API Key

Add your Cerebras API key:  
- `.env` file: `CEREBRAS_API_KEY=your_api_key_here`  
- Environment: `export CEREBRAS_API_KEY=your_api_key_here`

## Examples

**CLI Chat**  
```bash
./cerebras_cli --model qwen-3-32b --prompt "You are a helpful assistant."
```

**Web UI**  
```bash
./cerebras_server
# Open http://localhost:8080
```

## Troubleshoot

**Build Issues**  
- Missing headers? Install dependencies.  
- nlohmann/json missing? Run `brew install nlohmann-json` or `sudo apt install nlohmann-json3-dev`.  
- libcurl errors? Verify `curl` installation.  

**Runtime Issues**  
- API key errors? Check `.env` or environment variable.  
- Connection issues? Confirm internet and Cerebras API status.  
- Web UI not updating? Rebuild after modifying HTML/CSS/JS.  

## Project Structure

- `cerebras_cli.cpp`: CLI for chat requests  
- `cerebras_server.cpp`: Web server for UI and API  
- `index.html`, `styles.css`, `script.js`: Web UI components  
- `CMakeLists.txt`: Build configuration  
- `.env`: API key storage  

## Why Cerebras?

- **Speed**: 2,400 tokens/second  
- **Power**: Surpasses GPT-4.1 and Claude Sonnet 3.7  
- **Flexibility**: Hybrid reasoning, agentic workflows  
- **Openness**: Fully customizable open-weight model  
- **Ready**: Production-grade performance  

**Build the future.** Harness Cerebras to create, innovate, and inspire.
