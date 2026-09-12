# promptpipe-x

Minimal LLM CLI: stdin in, streamed answer out

Side project, maintained when I have time.

## Installation

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=sk-...
```

## What it does

- Works with any OpenAI-compatible endpoint
- Streams tokens as they arrive
- Reads the prompt from args or stdin
- Model and system prompt via flags or env

## How to use

```bash
chatsh explain this error < error.log
cat diff.patch | chatsh review this diff
```

## Project structure

```text
├── .github/
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── configuration.md
│   ├── development.md
│   ├── faq.md
│   ├── roadmap.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── tests/
│   └── test_smoke.py
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── chatsh.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## License

MIT. Do whatever you want.
