# AI Prompts & Agents Collection

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Prompts](https://img.shields.io/badge/Prompts-110-green.svg)](#prompt-packs)
[![Agents](https://img.shields.io/badge/Agents-28-purple.svg)](#agent-packs)

A free, open-source collection of high-quality AI prompts and agent configurations for developers. Battle-tested, model-agnostic, and ready for production use.

**Website**: [engels.wtf/prompts](https://www.engels.wtf/prompts)

## Quick Start

```bash
# Clone the repository
git clone https://github.com/engelswtf/ai-prompts.git

# Or download specific packs
curl -O https://raw.githubusercontent.com/engelswtf/ai-prompts/main/prompts/debugging/01-error-trace-analyzer.yaml
```

## Prompt Packs

| Pack | Prompts | Description |
|------|---------|-------------|
| [Debugging](prompts/debugging/) | 19 | Error analysis, stack traces, memory leaks, race conditions |
| [Code Review](prompts/code-review/) | 17 | Security scanning, performance review, code smells, PR summaries |
| [Documentation](prompts/documentation/) | 18 | READMEs, API docs, changelogs, architecture docs |
| [Config Translator](prompts/config-translator/) | 20 | Docker↔K8s, JSON↔YAML, CI/CD converters |
| [Security Audit](prompts/security-audit/) | 18 | OWASP scanning, auth review, dependency checks |
| [Log Analysis](prompts/log-analysis/) | 18 | Log summarization, anomaly detection, timeline reconstruction |

**Total: 110 prompts**

## Agent Packs

| Pack | Agents | Description |
|------|--------|-------------|
| [Infrastructure](agents/infrastructure/) | 7 | Storage Manager, VM Monitor, Security Auditor, Backup Manager, Network Monitor, Container Orchestrator, Database Admin |
| [Development](agents/development/) | 7 | Code Builder, DevOps Helper, Code Reviewer, Test Engineer, API Designer, Performance Engineer, Refactoring Expert |
| [Content](agents/content/) | 6 | Blog Writer, Documentation Writer, Social Media Writer, Newsletter Writer, Video Script Writer, Copy Editor |
| [Research](agents/research/) | 8 | Market Researcher, Competitor Analyst, Tech Scout, Literature Reviewer, Trend Analyst, User Researcher, Data Analyst, Fact Checker |

**Total: 28 agents**

## Format

### Prompts
Each prompt uses YAML frontmatter + markdown:

```yaml
---
id: error-trace-analyzer
name: Error Trace Analyzer
version: "1.0.0"
author: engels.wtf
license: MIT
category: debugging
tags: [error, stack-trace, debugging]
model_compatibility: [claude, gpt-4, gemini, llama]
---

# Error Trace Analyzer

## Role
[Expert persona description]

## Task
[What to do]

## Input
{{error_message}}

## Output Format
[Expected structure]

## Constraints
- DO [positive behavior]
- DO NOT [negative behavior]

## Examples
[Input/output demonstrations]
```

### Agents
Full system prompts in markdown:

```markdown
---
id: code-builder
name: Code Builder
version: "1.0.0"
...
---

# Code Builder

Expert development agent for building production-ready code...

## Role
[Detailed role description]

## Critical Rules
[Non-negotiable behaviors]

## Workflow
[Step-by-step process]
```

## Usage

### With ChatGPT / Claude / Gemini
1. Copy the prompt content (everything after the YAML frontmatter)
2. Replace `{{variable}}` placeholders with your actual data
3. Paste into your AI interface
4. Get consistent, high-quality results

### With Claude Projects / Custom GPTs
1. Use the agent markdown as a system prompt
2. The agent will follow its specialized behavior
3. Customize as needed for your specific use case

### Programmatic Use
```python
import yaml

with open('prompts/debugging/01-error-trace-analyzer.yaml') as f:
    content = f.read()
    # Split frontmatter and content
    parts = content.split('---')
    metadata = yaml.safe_load(parts[1])
    prompt = parts[2].strip()
    
    # Use the prompt
    prompt_filled = prompt.replace('{{error_message}}', your_error)
```

## Model Compatibility

All prompts are tested with:
- **Claude** (Sonnet, Opus)
- **GPT-4** / **GPT-4o**
- **Gemini Pro**
- **Llama 3** (70B+)

Some prompts may work with smaller models but results may vary.

## Contributing

Contributions welcome! Please:

1. Follow the existing format (YAML frontmatter + markdown)
2. Test your prompt with at least 2 different AI models
3. Include realistic examples in your prompt
4. Submit a PR with a clear description

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

## License

MIT License - use these prompts anywhere, modify freely, no attribution required.

## Acknowledgments

- Prompt engineering research from MIT, Anthropic, and OpenAI
- Inspiration from [awesome-chatgpt-prompts](https://github.com/f/awesome-chatgpt-prompts)
- [PatrickJS/awesome-cursorrules](https://github.com/PatrickJS/awesome-cursorrules) for cursor rules patterns

---

Made with ❤️ by [engels.wtf](https://www.engels.wtf)
