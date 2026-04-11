# Contributing

Thanks for helping improve this list.

## How to contribute

1. Open an issue with the `🎉 Addition to list` template, or open a PR directly.
2. Add your entry to both files:
   - `README.md`
   - `README.zh.md`
3. Keep changes focused. One app per PR is preferred.

### AI-assisted contributions

AI-assisted PRs are welcome, but contributors are still responsible for the final result.

This repository provides the repo-local skill [`awesome-swift-macos-apps-docs`](../.codex/skills/awesome-swift-macos-apps-docs/SKILL.md) for curation work.

It is intended for:
- Adding app entries to the bilingual READMEs: `README.md` and `README.zh.md`
- Updating existing listings in both files
- Adjusting category placement when an app belongs in a better section
- Keeping descriptions concise, one-sentence, and semantically aligned across both languages

Example prompt:

```text
Use $awesome-swift-macos-apps-docs

AppName
https://github.com/owner/repo

Add it to the English and Chinese docs with a concise one-sentence description. Do not emphasize that it is a macOS app.
```

- Review category placement before submitting. The closest comparable entries in the repo should guide the category choice.
- Update both `README.md` and `README.zh.md` together.
- Keep English and Chinese descriptions to one sentence each.
- Keep wording concise, factual, and focused on what the app is.
- Do not over-emphasize that the project is a macOS app unless that detail is required for clarity.
- Do not submit bulk AI-generated rewrites or unrelated cleanup.
- Verify the final placement and wording with `rg -n` and review `git diff` before opening the PR.

If you use a repo-local Codex skill or prompt template, make sure the output still follows the rules in this document and the PR template.

## What can be added

- Open-source apps written in Swift.
- Projects should be active and useful to end users or developers.
- The repository should have a clear README and a valid license.

## Entry format

Use the same format as existing items:

```md
- [AppName](https://github.com/owner/repo) <img align="bottom" height="13" src="https://badgen.net/github/stars/owner/repo?style=flat&label=" /> <img align="bottom" height="13" src="https://img.shields.io/github/last-commit/owner/repo?style=flat&label=" /> - One-sentence description.
```

## Writing rules

- Keep descriptions concise: one sentence.
- Describe what the app does, not marketing copy.
- Do not over-emphasize platform wording like "macOS app" unless needed for clarity.
- Keep tone neutral and factual.
- Prefer describing the app's core function over listing multiple features.

## Category rules

- Place entries in the most relevant category.
- If multiple categories could fit, choose the primary use case.
- Match the local section structure in each file instead of assuming both files are identical.
- Keep nearby ordering style consistent with the existing section.
- Do not move or rewrite neighboring entries unless needed for the requested change.

## Bilingual sync

- Every addition or edit in `README.md` must be mirrored in `README.zh.md`.
- Keep English and Chinese descriptions semantically aligned.
- Do not translate mechanically; keep the wording natural in each language.

## Update existing entries

When editing an existing app:

- Fix broken links or badge paths.
- Improve unclear descriptions while keeping them short.
- Avoid unrelated reformatting.

## PR checklist

- [ ] Added/updated in both `README.md` and `README.zh.md`
- [ ] Correct category
- [ ] Placement follows the local section structure in each file
- [ ] Ordering is consistent with nearby entries
- [ ] Description is one concise sentence
- [ ] English and Chinese descriptions are semantically aligned
- [ ] App entry appears once per intended file
- [ ] Link and badges are valid
- [ ] Checked final locations with `rg -n`
- [ ] Reviewed `git diff` for only intended listing changes
- [ ] No unrelated changes
