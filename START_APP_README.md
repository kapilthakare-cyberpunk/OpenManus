# OpenManus Application

Welcome to OpenManus, an AI-powered agent application configured to work with local Ollama models.

## Prerequisites

Before running the application, ensure you have:

1. **Ollama installed and running** on your system
2. **Required models** pulled to your local system (e.g., `llama3.2`, `llava`)
3. **Python 3.12** environment

## Quick Start

### Method 1: Using the start script (recommended)
```bash
# Navigate to the project directory and run:
./start-app

# Or provide a prompt directly:
./start-app "What can you help me with today?"
```

### Method 2: Direct execution
```bash
# Run without a prompt (will prompt for input):
python main.py

# Or run with a prompt:
python main.py --prompt "Your prompt here"
```

## Configuration

The application is pre-configured to use your local Ollama installation:

- **LLM Provider**: Ollama
- **Model**: llama3.2 (default)
- **Endpoint**: http://localhost:11434/v1
- **Vision Model**: llava (for image processing)

To change the model, edit the `config/config.toml` file and modify the `model` parameter in the `[llm]` section.

## Troubleshooting

### Common Issues:

1. **"Ollama server not responding"**: Make sure Ollama is running by executing `ollama serve` in a separate terminal.

2. **Missing models**: Pull required models with:
   ```bash
   ollama pull llama3.2
   ollama pull llava  # for vision capabilities
   ```

3. **Dependency errors**: Ensure all dependencies are installed:
   ```bash
   pip install -r requirements.txt
   ```

## Features

- Local AI model processing using Ollama
- Vision capabilities with llava model
- Browser automation and interaction
- Tool calling capabilities
- MCP (Model Context Protocol) integration
- Data analysis agent support

## Notes

- The application uses your local models, so no external API keys are required
- All processing happens locally on your machine
- Make sure your system meets the requirements for running the selected models