---
name: awesome-swift-macos-apps-docs
description: Use when adding, updating, or validating app entries in the awesome-swift-macos-apps repository, especially when maintaining both README.md and README.zh.md with concise one-sentence descriptions, correct category placement, and consistent bilingual formatting.
---

# Awesome Swift macOS Apps Docs

Use this skill when the task is to maintain app entries in this repository's bilingual docs.

## Use this skill for

- Adding a new app entry to `README.md` and `README.zh.md`
- Updating an existing app entry in both files
- Fixing wrong links, duplicate entries, inconsistent descriptions, or mismatched category placement
- Moving an existing app entry to a better category while preserving local document structure
- Keeping reply format consistent for this repository

Do not use this skill for code changes in other projects.

For supported files and default scope boundaries, see [references/supported-files.md](references/supported-files.md).
For category-specific notes and placement heuristics, see [references/category-notes.md](references/category-notes.md).

## Repository Targets

Always update both files together:
- `README.md`
- `README.zh.md`

## Core workflow

1. Identify the most appropriate category by searching existing README files for similar apps or keywords.
2. Read the local context around the target section in both languages before editing.
3. Check whether the app already exists in either file.
4. Add or update both entries together.
5. Keep the description to one sentence in each language.
6. Verify placement, wording, and formatting with `rg` and `git diff`.

## Entry Rules

For each new app entry:
- Use a single concise sentence to describe what the app is
- Prefer describing the core function, not a feature list
- Do not emphasize that it is a macOS app unless that is essential to understanding the app
- Keep English and Chinese descriptions aligned in meaning, but do not translate mechanically
- Preserve existing markdown format, badges, and ordering style used in the target section
- Keep naming consistent with the user's request; if the repo name differs from the display name, follow the user's requested display name unless there is a strong reason not to

## Curation Rules

- Match the local section used by each document instead of assuming both files are structured identically.
- Preserve existing ordering within a section. In practice this is usually alphabetical by app name or grouped with similar nearby tools.
- Do not rewrite neighboring entries unless needed for the requested task.
- Keep edits narrowly scoped to the requested listing work.

## Category Placement

Choose the closest existing category based on the app's main purpose.

Heuristics:
- AI clients, coding-agent dashboards, AI utilities: `AI`
- Local model runtimes and model-serving tools: `Local LLM`
- Terminal environments, multiplexers, SSH/native shell workspaces: `Terminal`
- Docker-based local web/dev stack tools: `Web Development`
- Git identity/config/dev helper tools: `Other Development`
- Window tiling, snapping, positioning: `Window Management`
- Clipboard tools: `Clipboard`
- Audio/video players: `Player`
- Keyboard layout/input overlays: `Keyboard`
- Screenshot/OCR/capture tools: screenshot-related section already present in main list; place near similar entries
- If no category is clearly better, use `Other`

When unsure, inspect nearby entries before editing.

## Description Style

English:
- Short and direct
- Prefer noun-phrase or simple functional sentence fragments
- Avoid marketing words like "powerful", "beautiful", "premium", "ultimate" unless needed for meaning
- Avoid long feature enumerations

Chinese:
- Keep it natural and concise
- Prefer patterns like `用于…的工具` / `…管理工具` / `…客户端` / `…工作台`
- Do not force exact word order from English

Preferred patterns:

- `Git identity manager for switching profiles, emails, and SSH keys.`
- `SSH workspace for Hermes with sessions, files, usage, skills, and a real terminal.`
- `集截图、录屏、标注、OCR 和贴屏展示于一体的工具。`

## Validation

- Search for the app name in `README.md` and `README.zh.md`
- Review `git diff` for only the intended changes
- Confirm the entry appears once per intended file
- Confirm the wording remains one sentence in each language
- Confirm final line numbers with `rg -n`

## Reply Format

After finishing, reply briefly with:
- whether it was added or updated
- English file location
- Chinese file location
- final English description
- final Chinese description
- whether tests were run; for doc-only changes, say tests were not run

## Notes

Common user preference for this repository:
- "描述简明扼要"
- "一句话说明是个什么应用"
- "不要强调 macOS 应用" unless the user explicitly asks otherwise

## Scope Boundary

- This skill is for repository curation, not for rewriting repository structure or reformatting unrelated content.
- If the user asks for a broader taxonomy change, inspect the surrounding sections first and then make the smallest consistent change.
