# MODELS.md -- LLM Uebersicht & Empfehlungen

_Abfragbar via /llm oder /llms_

## Alle Modelle (44 Modelle, 44 Aliases)

### Anthropic (3)
- `opus` -- anthropic/claude-opus-4-6 ($$$, 195k ctx)
- `sonnet` -- anthropic/claude-sonnet-4-6 ($$, 195k ctx)
- `copilot-sonnet45` -- anthropic/claude-sonnet-4-5 ($$, 195k ctx)

### OpenAI Codex (7)
- `chatgpt` -- openai-codex/gpt-5.3-codex ($$, 266k ctx)
- `chatgpt-spark` -- openai-codex/gpt-5.3-codex-spark ($$, 266k ctx)
- `gpt52` -- openai-codex/gpt-5.2 ($$, 266k ctx)
- `gpt52c` -- openai-codex/gpt-5.2-codex ($$, 266k ctx)
- `gpt51` -- openai-codex/gpt-5.1 ($$, 266k ctx)
- `gpt51-max` -- openai-codex/gpt-5.1-codex-max ($$, 266k ctx)
- `gpt51-mini` -- openai-codex/gpt-5.1-codex-mini ($$, 266k ctx)

### Google Gemini (9)
- `gemini` -- google-gemini-cli/gemini-3-pro-preview (1M ctx)
- `gemini-flash` -- google-gemini-cli/gemini-3-flash-preview (1M ctx)
- `gemini31` -- google-gemini-cli/gemini-3.1-pro-preview (1M ctx)
- `gemini25` -- google-gemini-cli/gemini-2.5-pro (1M ctx)
- `gemini25-flash` -- google-gemini-cli/gemini-2.5-flash (1M ctx)
- `gemini25-flash-preview` -- google-gemini-cli/gemini-2.5-flash~preview (1M ctx)
- `gemini20-flash` -- google-gemini-cli/gemini-2.0-flash (1M ctx)
- `nano-banana` -- google-gemini-cli/gemini-2.5-flash-image (Bildgenerierung)
- `nano-banana-pro` -- google-gemini-cli/gemini-3-pro-image-preview (Bildgenerierung)

### GitHub Copilot (23, alle FREE)
- `copilot-opus` -- github-copilot/claude-opus-4.6
- `copilot-opus45` -- github-copilot/claude-opus-4.5
- `copilot-sonnet46` -- github-copilot/claude-sonnet-4.6
- `copilot-sonnet` -- github-copilot/claude-sonnet-4.5
- `copilot-sonnet4` -- github-copilot/claude-sonnet-4
- `haiku` -- github-copilot/claude-haiku-4.5
- `copilot52` -- github-copilot/gpt-5.2
- `copilot52c` -- github-copilot/gpt-5.2-codex
- `copilot-gpt51` -- github-copilot/gpt-5.1
- `copilot51` -- github-copilot/gpt-5.1-codex
- `copilot-max` -- github-copilot/gpt-5.1-codex-max
- `copilot51-mini` -- github-copilot/gpt-5.1-codex-mini
- `gpt5` -- github-copilot/gpt-5
- `gpt5mini` -- github-copilot/gpt-5-mini
- `copilot-gpt41` -- github-copilot/gpt-4.1
- `copilot-4o` -- github-copilot/gpt-4o
- `copilot-gemini` -- github-copilot/gemini-3-pro
- `copilot-gemini-preview` -- github-copilot/gemini-3-pro-preview
- `copilot-gemini25` -- github-copilot/gemini-2.5-pro
- `copilot-gemini31` -- github-copilot/gemini-3.1-pro-preview
- `copilot-flash` -- github-copilot/gemini-3-flash
- `copilot-flash-preview` -- github-copilot/gemini-3-flash-preview
- `grokfast` -- github-copilot/grok-code-fast-1

### Perplexity (2)
- `sonar` -- perplexity/sonar-pro (Web-Suche mit Quellen)
- `deep` -- perplexity/sonar-deep-research (Tiefenanalyse)

## AAHP v3 Empfehlung

Faustregel: **Teuer denken, billig ausfuehren.**

**Planning:** `copilot-opus` (FREE)
**Coding:** `copilot52c` / `grokfast` (FREE)
**Review:** `copilot-sonnet46` (FREE)
**Triage:** `haiku` (FREE)
**Bulk:** `copilot-flash` (FREE)
**Research:** `gemini25` (1M ctx) / `sonar` (Web)
**Bilder:** `nano-banana` / `nano-banana-pro`
**Fallback:** `gemini25-flash` (billigst mit Qualitaet)

## Kosten-Tipp

23 von 44 Modellen sind FREE via GitHub Copilot Abo.
Wo moeglich IMMER Copilot-Variante bevorzugen!

---
_Stand: 2026-02-28 -- 44 Modelle, 44 Aliases_
