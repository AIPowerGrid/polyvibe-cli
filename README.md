# PolyVibe CLI

<div align="center">

**AI-powered coding assistant for Polygon dApp development**

*Forked from [qwen-code](https://github.com/QwenLM/qwen-code), customized for Web3*

</div>

## What's New in PolyVibe CLI

- **Local model support** (GPT OSS 120B, Ollama, LM Studio, etc.)
- **Polygon-optimized** for dApp development
- **Commands**: `polyvibe` or `pv` for quick access
- **DashScope Intl** support for Qwen models

## Quick Start with DashScope

### 1. Get your DashScope API key

Sign up at [DashScope International](https://dashscope.aliyuncs.com/) and get your API key.

### 2. Configure environment

Edit `.env.example` to `.env` and add your key:

```env
OPENAI_API_KEY=your-dashscope-api-key
OPENAI_BASE_URL=https://dashscope-intl.aliyuncs.com/compatible-mode/v1
OPENAI_MODEL=qwen3-coder-plus
```

### 3. Run PolyVibe CLI

```bash
cd /Users/j/polyvibe-cli/cli
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

### Using Different Models

Edit `.env` to switch models:

**Ollama:**
```env
OPENAI_BASE_URL=http://localhost:11434/v1
OPENAI_MODEL=llama3
```

**LM Studio:**
```env
OPENAI_BASE_URL=http://localhost:1234/v1
OPENAI_MODEL=your-model-name
```

**Local GPT OSS 120B:**
```env
OPENAI_API_KEY=sk-no-key-required
OPENAI_BASE_URL=http://localhost:8080/v1
OPENAI_MODEL=gpt-oss-120b
```

**DashScope Intl (Qwen models):**
```env
OPENAI_API_KEY=your-dashscope-api-key
OPENAI_BASE_URL=https://dashscope-intl.aliyuncs.com/compatible-mode/v1
OPENAI_MODEL=qwen3-coder-plus
```

**Cloud (OpenAI):**
```env
OPENAI_API_KEY=your-actual-api-key
OPENAI_BASE_URL=https://api.openai.com/v1
OPENAI_MODEL=gpt-4
```

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
├── .env              # Local configuration
└── README.md         # This file
```

## Troubleshooting

### CLI not connecting to model
1. Check if your model is running: `curl http://localhost:8080/v1/models`
2. Verify the endpoint in `.env`
3. Check the model name matches exactly

### Node version warning
PolyVibe requires Node.js 20+. Current version: 18.x
```bash
# Update Node.js (recommended)
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
