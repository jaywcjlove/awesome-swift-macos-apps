# Supported Files

This skill is primarily for the repository's bilingual app listings.

## Default targets

- `README.md`
- `README.zh.md`

These are the default files for app additions, removals, description updates, and category moves unless the user explicitly asks to touch a different document set.

## Working assumptions

- The two README files are related, but their local section structure may differ.
- English placement does not guarantee identical placement in Chinese.
- When local structure differs, preserve the established structure in each file.

## Included work

- Add a new app listing.
- Update an existing listing description.
- Reclassify an app into a better category.
- Normalize link or badge formatting for the touched entry.
- Verify final locations and touched lines for the updated entry.

## Excluded by default

- `docs/CONTRIBUTING.md`
- `docs/PULL_REQUEST_TEMPLATE.md`
- Other files under `docs/`
- Files under `.codex/skills/`

Do not touch these files unless the user explicitly asks for repository-maintainer rule changes, contributor workflow changes, or skill updates.

## Placement rule

Use the closest comparable apps already present in the target section as the primary signal for where a new entry belongs.

## Editing boundary

Keep edits tightly scoped to the requested listing work. Avoid unrelated cleanup, bulk reformatting, or section rewrites unless the user explicitly asks for them.
