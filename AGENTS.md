# AGENTS.md

Guidance for AI agents (and humans) reviewing or changing this repository.

This repo is an Awesome List for [Trystero](https://github.com/dmotz/trystero)
resources. Almost every change is a new entry in `README.md`, so the rules
below are about keeping entries consistent and valid.

## Entry format

Each entry is a single Markdown list item:

```md
- [Name](https://project-url/) [[source code](https://github.com/owner/repo)] - A short description.
```

- Omit the `[[source code](...)]` part if the project has no public source.
- Match the formatting of the surrounding entries.
- Keep the description short and factual.

## Alphabetical order

Each section in `README.md` (marked with a `MUST be listed in alphabetical
order` comment) must stay sorted alphabetically by entry name.

- Compare names case-insensitively (e.g. `Tenebra` < `WebChat` < `xrfragment`).
- When adding an entry, check its neighbors in the full list on the base
  branch, not just the lines in the diff.
- If an existing entry is out of order, point it out rather than silently
  reordering unrelated entries in the same PR.

## Link verification

Every link added or changed in a PR must be checked before approving or merging.

- Request each URL (for example with `curl -sSL -o /dev/null -w '%{http_code}'`)
  and expect a successful (2xx) final response after redirects.
- Some sites (e.g. `github.com`) may return 403 to automated clients or
  through a sandbox proxy. That is not proof the link is broken. Report the
  link as "unverified", not as "working" or "broken", and ask a human to open
  it.
- Do not claim a link works unless you actually checked it.
- Confirm the source-code link points to the same project as the main link.

## Reviewing PRs

When reviewing an entry PR, report:

1. Whether the entry is in the correct alphabetical position.
2. The result of each link check, noting any that could not be verified.
3. Whether the entry matches the format above and the PR touches only the
   intended line(s).

Don't make claims you haven't verified (for example, that a project uses a
particular Trystero strategy) without saying they are unchecked.

## Pull requests

- One project per PR, so each can be reviewed and merged independently.
- Don't reformat or reorder unrelated parts of `README.md`.
