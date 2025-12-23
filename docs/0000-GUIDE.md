# LLM Collaboration Guide for metabolic-protocols

If you are reading this, you are an LLM (likely Claude) being invoked in this repository. This document contains context and preferences learned from previous sessions to help you work effectively with this user.

## Project Overview

This is a collection of LCHF (Low-Carb High-Fat) recipe protocols in Markdown format. The user is diabetic and follows a strict low-carb diet. Recipes are located in `src/protocols/` and follow a consistent structure with YAML frontmatter.

## User Preferences

### Communication Style
- **Be direct and technical.** User appreciates detailed explanations with the science/rationale behind recommendations.
- **Use tables liberally.** User finds tabular data easy to parse (blanching times, salt amounts, troubleshooting guides).
- **Correct misinformation.** User has consulted other LLMs (Gemini) and appreciates when you respectfully correct inaccurate advice with proper reasoning.
- **Humor is welcome.** User has a dry sense of humor and appreciates light banter (e.g., jokes about 80s nutrition advice).

### Working Pattern
- **Iterative refinement.** User discusses issues encountered when cooking, then asks for recipe updates.
- **Batch commits.** User prefers to work through multiple recipes in one session, then commit all changes together at the end.
- **Descriptive commits.** Include bullet points summarizing what changed in each file.
- **Push when asked.** Don't push automatically; wait for explicit instruction.

### Recipe Format Preferences
- **Protocol Overview** section at top explaining the approach
- **Ingredients** organized into logical subsections (Base, Optional Add-ins, Toppings, etc.)
- **Execution Protocol** with numbered steps
- **Troubleshooting tables** at the end showing Problem → Cause → Fix
- **Notes/Options sections** for alternatives (e.g., Swerve vs Allulose)
- **Preparation and Timing sections** when advance prep is needed

### Technical Details Learned

| Topic | User's Situation |
|-------|------------------|
| **Diet** | LCHF/Keto, diabetic, strict carb counting |
| **Location** | Plano, TX - shops at HEB |
| **Sweeteners** | Has Confectioner's Swerve (special ordered), also has Allulose |
| **Equipment** | GreenPan ceramic waffle maker (full-size, 4-segment), stand mixer, no double boiler (has steamer with holes) |
| **Preferences** | Dislikes fennel (too strong), wife dislikes mushrooms and cream |

### Cooking Issues Previously Addressed

1. **Allulose browning** - Browns excessively in baked goods due to Maillard reaction at lower temps. Solution: Use Swerve instead, or accept cosmetic browning.

2. **Stuffing too dense** - Ground turkey + egg + parmesan over-binds into meatball texture. Solution: Add crushed pork rinds, reduce egg/parmesan, don't mix until tacky.

3. **Green beans too crisp** - 5 minutes blanching insufficient. Solution: 8-15 minutes depending on bean type and desired texture.

4. **Chaffle tastes like cardboard** - Part-skim mozzarella + no salt = bland. Solution: Use cheese blend, add salt, add butter, use full-fat only.

5. **Sauce too thin** - Cream not reduced enough. Solution: Reduce cream first, add cream cheese for body, increase parmesan.

### Sweetener Quick Reference

| Sweetener | Substitution | Notes |
|-----------|--------------|-------|
| Confectioner's Swerve | 1:1 with sugar/allulose | Contains tapioca starch (~0.5g carb/Tbsp), no browning, no recrystallization |
| Granular Swerve | 1:1 with sugar/allulose | Can recrystallize when chilled (gritty texture) |
| Allulose | 1:1 with sugar | True zero-carb, but browns excessively when baked |

### Repository Conventions

- Recipes live in `src/protocols/*.md`
- YAML frontmatter includes: title, tags, macros (carbs/fat/protein), prep_time, cook_time
- Times use ISO 8601 duration format (e.g., `PT20M` for 20 minutes)
- Commit messages use prefixes: `feat:`, `update:`, `fix:`
- Session logs go in `session-log.md` (gitignored)

## When Starting a New Session

1. Read this guide first
2. Ask what recipes the user wants to discuss
3. Read those recipe files before making suggestions
4. Discuss changes conversationally before editing
5. Make edits when user approves
6. Commit and push only when explicitly asked

## Session Log

Append to `session-log.md` (in repo root, gitignored) at the end of each session with:
- Date and time
- Model/interface used
- Summary of changes
- Commit hashes

---

*Last updated: December 23, 2025 by Claude Opus 4.5*
