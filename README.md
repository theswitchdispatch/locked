# Natal Chart Analysis Tool — A Grounded Method

A lightweight, single-file web tool for running a structured personality analysis using a natal chart as the starting point. Treats astrology as a symbolic vocabulary for pattern recognition — not prediction, not fate. Layers Jungian psychology on top to explain the mechanisms behind the patterns.

**Live tool → [](https://github.com)**

---

## What it does

Most natal chart tools output horoscope-style descriptions. This one is different. It gives you:

- A structured three-prompt sequence designed for Claude or ChatGPT
- Step-by-step instructions for generating and saving your natal chart PDF
- Prompt 1 — symbolic personality analysis (tensions, behavioural patterns, accuracy check)
- Prompt 2 — Jungian archetypal layer (Shadow, Ego, Persona, individuation arc)
- Prompt 3 — synthesis into a practical operating model with an interruptible behavioural loop

The output is a practical profile, not a horoscope. The framing explicitly asks the model to flag where astrology is accurate, where it's overstated, and where it's noise.

---

## How to use it

### Step 0 — Get your natal chart

1. Go to **[astro.cafeastrology.com/natal.php](https://astro.cafeastrology.com/natal.php)**
2. Enter your birth date, exact time, and place of birth
3. Use browser Print (Cmd+P / Ctrl+P) → **Save as PDF**
4. Save the full page — chart wheel, planet table, house cusps, aspects, and interpretations

### Step 1 — Run the analysis

1. Open **[Claude](https://claude.ai)** or **[ChatGPT](https://chat.openai.com)**
2. Attach the saved PDF
3. Copy and send **Prompt 1** from the tool
4. In the same session, send **Prompt 2** (Jungian layer) — no need to re-attach the PDF
5. Optionally send **Prompt 3** to synthesise both into an operating model

---

## The three prompts

### Prompt 1 — Natal Chart Interpretation

> Analyse the chart as a symbolic personality model. Extract core tensions, translate into behavioural patterns, flag what's accurate vs. noise, and reframe into a practical profile. Pattern-matching, not cosmic truth.

### Prompt 2 — Jungian Archetypal Layer

> Run a Jungian interpretation: Ego, Shadow, Persona, Anima/Animus, the four functions (Thinking, Feeling, Sensation, Intuition), and the individuation arc. Focus on *why* the patterns exist — the mechanism, not just the description.

### Prompt 3 — Operating Model Synthesis

> Synthesise both analyses into a practical operating model. Describe the default behavioural loop, make it interruptible, give 3–4 in-the-moment rules, and write one synthesis sentence.

All three prompts are available in the tool with one-tap copy buttons.

---

## Design notes

- **Single file** — no dependencies, no build step, no backend. Drop `index.html` anywhere and it works.
- **Mobile-first** — fully responsive down to 375px. Copy buttons are full-width on mobile, prompt blocks wrap cleanly, tap targets are sized for thumbs.
- **No tracking, no data collection** — nothing is sent anywhere. The tool is purely a prompt delivery mechanism.
- **Typography** — Cormorant Garamond (display) + DM Sans (body), loaded from Google Fonts.

---

## Files

| File | Description |
|------|-------------|
| `index.html` | The tool — rename `birth-chart-tool.html` to this for GitHub Pages |
| `README.md` | This file |

---

## Running locally

No setup needed. Just open `index.html` in any browser.

```bash
# Clone the repo
git clone https://github.com/yourusername/your-repo-name.git

# Open directly
open index.html
```

---

## Notes on methodology

This tool was built around a specific insight: **description tells you what you are; a mechanism tells you where to intervene.** The two-prompt structure (astrology → Jungian) is designed to move from pattern naming to psychological mechanism — which changes how you work on the patterns.

A few things worth knowing before you run it:

- **Birth time matters.** Even 15 minutes can shift the Ascendant sign. If you don't know your exact time, use 12:00 noon but treat the Ascendant as unreliable.
- **Two models, different strengths.** Claude tends to go deeper on mechanism and origin. ChatGPT tends to produce tighter loops and failure modes. Running both and comparing is worth the effort.
- **Flag the noise explicitly.** Without the instruction to flag overstated or symbolic-only claims, models will default to flattery. The prompts in this tool include that instruction.
- **The Shadow analysis is the most actionable layer.** It reframes habitual behaviours as psychological mechanisms rather than personality traits — which changes what you do about them.

---

## Licence

MIT — use, adapt, share freely. Not medical or psychological advice.
