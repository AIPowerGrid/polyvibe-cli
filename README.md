# PolyVibe CLI

<div align="center">

**AI-powered coding assistant for Polygon dApp development**

*Forked from [qwen-code](https://github.com/QwenLM/qwen-code), customized for Web3*

</div>

## What's New in PolyVibe CLI

- **OpenAI-compatible API support** (works with any OpenAI-compatible endpoint)
- **Local model support** (Ollama, LM Studio, vLLM, LocalAI, etc.)
- **Polygon-optimized** for dApp development
- **Commands**: `polyvibe` or `pv` for quick access

## Quick Start

### 1. Install dependencies

```bash
npm install
```

### 2. Configure your model

Copy `.env.example` to `.env` and configure your model endpoint:

```bash
cp .env.example .env
```

Edit `.env` with your model settings (see Configuration section below).

### 3. Run PolyVibe CLI

```bash
npm start
```

Or install globally:

```bash
npm link
polyvibe  # or just: pv
```

## Usage Examples

### Start a conversation
```bash
polyvibe
# or
pv
```

### With a specific prompt
```bash
polyvibe "Help me create a Polygon NFT contract"
```

### Available commands in the CLI
- `/help` - Show available commands
- `/clear` - Clear conversation
- `/settings` - Configure model settings
- `/polygon` - Polygon development help
- `/exit` - Exit PolyVibe

## Configuration

PolyVibe CLI works with any OpenAI-compatible API endpoint. Edit `.env` to configure your model:

```env
OPENAI_API_KEY=your-api-key
OPENAI_BASE_URL=http://localhost:11434/v1  # or your endpoint
OPENAI_MODEL=your-model-name
```

Works with: Ollama, LM Studio, vLLM, LocalAI, OpenAI, or any OpenAI-compatible API.

See `.env.example` for additional configuration options including timeout, retry settings, and proxy configuration.

## Polygon Development

PolyVibe is optimized for Polygon dApp development with:
- Smart contract templates
- matic.js integration examples
- Best practices for gas optimization
- Mumbai testnet configuration

## Documentation

- [Main PolyVibe README](../README.md)
- [Development Setup](../DEVELOPMENT_SETUP.md)
- [Original qwen-code docs](https://qwenlm.github.io/qwen-code-docs/)

## Project Structure

```
cli/
├── packages/
│   ├── cli/          # CLI interface
│   ├── core/         # Core functionality
│   └── ...
├── bundle/           # Built CLI executable
├── .env.example      # Example configuration
└── README.md         # This file
```

## Troubleshooting

### CLI not connecting to model
1. Check if your model server is running
2. Verify the endpoint URL in `.env`
3. Check the model name matches your server's model

### Node version requirements
PolyVibe requires Node.js 20 or higher.
```bash
# Update Node.js
nvm install 20
nvm use 20
```

### Permission errors
```bash
sudo npm link  # If global install fails
```

## Contributing

See the main [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.

## License

Apache 2.0 - See [LICENSE](../LICENSE)

## Acknowledgments

Built on top of the excellent [qwen-code](https://github.com/QwenLM/qwen-code) project.

---

**AI-powered coding for Polygon dApp development**
