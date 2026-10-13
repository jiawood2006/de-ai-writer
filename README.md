# AI 文案去味器 · De-AI Writer

> Rewrite AI-sounding Chinese copy into text that reads like a human wrote it.

把 AI 生成的中文改写成**有真人味**的文字：专治空洞拔高、排比三连、官方黑话、模板化结尾。适用于公众号、小红书、电商文案、产品描述。

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/format-Agent%20Skill-2f6fed)](#install)
[![Part of](https://img.shields.io/badge/also%20in-hermes--skills%20collection-555)](https://github.com/jiawood2006/hermes-skills)

## Install

```bash
# 1) Agent Skills CLI (works with 50+ agent hosts)
npx skills add jiawood2006/de-ai-writer

# 2) Claude Code / any host that reads ~/.claude/skills
git clone https://github.com/jiawood2006/de-ai-writer.git ~/.claude/skills/de-ai-writer

# 3) Hermes Agent
git clone https://github.com/jiawood2006/de-ai-writer.git ~/.hermes/skills/utilities/de-ai-writer
```

No build step, no account, no telemetry.

## Usage

```bash
# A) with an API key (best quality) — any OpenAI-compatible endpoint
export LLM_API_KEY="sk-..."                      # or pass --api-key
export LLM_BASE_URL="https://api.deepseek.com/v1"
export LLM_MODEL="deepseek-chat"

python3 scripts/deai.py 稿子.txt -o 改好.txt      # rewrite a file
python3 scripts/deai.py 稿子.txt                  # print to stdout

# B) zero-cost mode — no API call at all, just prints a rewrite prompt you can paste anywhere
python3 scripts/deai.py 稿子.txt --prompt-only
```
Ask your agent: *"帮我把这段去一下 AI 味"* and it will drive the script for you.

## Requirements

Python 3.9+. **Zero third-party dependencies** (standard library only). `LLM_API_KEY` is optional — without it use `--prompt-only`.

## Notes

The zero-cost mode exists on purpose: you can evaluate the rewriting logic before spending a single token.

## License

MIT — see [LICENSE](LICENSE). Issues and PRs welcome.
Part of the [hermes-skills](https://github.com/jiawood2006/hermes-skills) collection.
