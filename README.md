# AI Prompts

A collection of production-ready system prompts for Claude.ai Projects. Each prompt is a complete agent specification — not a one-liner, not a template to fill in, but a fully-formed instruction set designed to produce consistent, high-quality outputs for specific use cases.

## What This Is

These are the prompts I actually use. They're published here because:
1. Other people asked for them
2. They're specific enough to be useful without customisation
3. They demonstrate what a well-structured agent prompt looks like

**These are not:**
- Generic ChatGPT prompt libraries
- Marketing copy generators
- "Act as X" one-liners that need you to fill in the details

**These are:**
- Complete system architectures for AI agents
- Opinionated about behaviour, tone, and output format
- Ready to paste into Claude.ai Project custom instructions
- Designed for repeated use, not one-off queries

## Philosophy

Most prompt repositories are catalogues. This one is a toolkit.

The prompts here prioritise:
- **Specificity over flexibility** — narrow, deep capability beats broad, shallow coverage
- **Constraints over open-endedness** — defining what *not* to do is as important as what to do
- **Consistent behaviour** — the same input should produce structurally similar outputs
- **Production use** — these are built for daily work, not experimentation

Each prompt includes:
- Role definition and persona
- Interaction patterns (how the agent engages)
- Output structure and formatting rules
- Explicit boundaries (what the agent refuses or redirects)
- Examples where ambiguity exists

## Available Prompts

### AI Cooking Assistant
**File:** [`prompts/cooking-assistant.md`](prompts/cooking-assistant.md)

A personalised sous chef that combines a sharp, Bourdain-inspired voice with deep knowledge of your kitchen equipment, local produce, and culinary reference library. Pushes your cooking further rather than just suggesting recipes.

**Use when:** You want an opinionated collaborator in the kitchen, not a recipe search engine.

**Integrates with:** [`ourgroceries-bridge`](https://github.com/PeteInBrissie/ourgroceries-bridge) for shopping list management.

**Template structure:** Fill in placeholders for household, location, equipment, cookbook library, and cooking philosophy to calibrate the agent to your actual context.

---

### The Comedic Explainer
**File:** [`prompts/oliver-explainer.md`](prompts/oliver-explainer.md)

A long-form explainer in the style of John Oliver's *Last Week Tonight*. Takes any topic and renders it as: meticulously researched, genuinely outraged, built to an absurd-but-accurate analogy ("And look—"), and willing to tell you it gets worse.

**Use when:** You need to understand a complex, under-explained, or deliberately obscured topic and want the explanation to be both rigorous and readable.

**Output format:** 500–1000+ word responses with structured argumentation, mandatory analogy section, and "it gets worse" beats for harmful systems.

**No customisation required:** Load as-is.

---

### The Prompt Generator
**File:** [`prompts/prompt-generator.md`](prompts/prompt-generator.md)

A prompt engineering specialist that converts topics into complete system prompts for other AI agents. Infers the role, defines constraints, specifies interaction patterns, and structures output expectations.

**Use when:** You need to create a new agent but don't want to write the prompt from scratch.

**Output format:** Complete "I want you to act as..." prompts with role declaration, context, constraints, examples, and explicit boundaries.

**No customisation required:** Load as-is.

---

### Japan Trip Planner
**File:** [`prompts/japan-guide.md`](prompts/japan-guide.md)

A Japan trip-planning agent for repeat visitors that tracks your visit history and curates deep-cut experiences around your specific interests. Skips tourist staples you've already seen and prioritises authenticity, local industries, and places that feel discovered rather than assigned.

**Use when:** You've been to Japan before and want to go deeper — second-visit experiences, specialist shops, regional day trips, and hyper-local recommendations aligned with your interests (car culture, manga/anime, food, craft, etc.).

**Template structure:** Fill in your visit history (cities visited once, twice, never) and interest areas. The agent adjusts recommendations based on whether you've been somewhere before.

**Response structure:** Organised into clear sections (Why Go, Deep-Cut Experiences, Specialist Shopping, Day Trips) with context for every recommendation — not just lists.

---

## How to Use These

### In Claude.ai Projects

1. Create a new Project in Claude.ai
2. Open Project settings → Custom instructions
3. Copy the entire contents of the `.md` file
4. Paste into the custom instructions field
5. Save

**For template prompts** (e.g., Cooking Assistant):
- Fill in all `[PLACEHOLDER]` sections before saving
- The more specific you are, the better the agent performs

**For ready-to-use prompts** (e.g., Explainer, Prompt Generator):
- Paste as-is, no changes needed
- Start using immediately

### In Other Contexts

These prompts are written for Claude but can be adapted for:
- **ChatGPT Custom GPTs:** Paste into instructions field
- **API system prompts:** Use as the system message in your API calls
- **Other AI platforms:** May require minor syntax adjustments

## Prompt Structure Principles

If you're building your own prompts, here's what makes these effective:

### 1. Role Definition
State what the agent *is* and what problem it solves. Not just "you are a writer" — specify the domain, the audience, the task.

### 2. Constraints Are Features
Define what the agent *doesn't* do. Boundaries prevent scope creep and maintain focus.

### 3. Interaction Patterns
How does the agent engage? Does it ask questions first? Provide options? Explain reasoning? Make recommendations?

### 4. Output Format
Be explicit. Prose vs bullet points? Length expectations? Required sections?

### 5. Tone Calibration
Formal, conversational, sarcastic, encouraging? Specify and provide examples.

### 6. Examples > Explanation
When behaviour is ambiguous, show what good looks like rather than describing it.

## Contributing

Not currently accepting contributions. This is a personal collection of prompts I use regularly — adding community submissions would change its purpose.

If you want to share a prompt you've built, consider:
- Forking this repo and publishing your own collection
- Opening a Discussion to share the prompt for others to see

## License

**CC0 1.0 Universal (Public Domain)**

These prompts are free to use, modify, and distribute without attribution. Do whatever you want with them.

## Related Projects

- **[ourgroceries-bridge](https://github.com/PeteInBrissie/ourgroceries-bridge)** — HTTP bridge connecting Claude to OurGroceries shopping lists, designed to work with the Cooking Assistant prompt

## About

Built and maintained by someone who got tired of generic AI responses and decided to fix it with better prompts.

If these are useful, great. If not, build your own.
