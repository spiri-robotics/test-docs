# Spiri Documentation Test Build

Testing spiri's documentation builds and system.

Document number **SPIRI-TEST-001**.

A **regulator-facing controlled document**. Every issued revision names an
approver and an effective date.

## Read it

- **Online:** <https://spiri-documentation-test-build.readthedocs.io>
- **PDF:** <https://github.com/spiri-robotics/spiri-documentation-test-build/releases/latest>

  The PDF attached to a release is the controlled copy. Link customers and
  regulators to it rather than to the Read the Docs PDF, which is rebuilt in place
  and can change after they have it.

## Edit it

**→ [CONTRIBUTING.md](CONTRIBUTING.md)** walks through it from nothing: which
two programs to install, how to preview your changes as you type, and how to
share them. No programming knowledge needed, and nothing to configure.

The short version, once you are set up: open the folder in VS Code, click
**Reopen in Container**, press `Ctrl+Shift+B`, and edit the `.md` files in
[`docs/`](docs/).

## What is where

| Path | What it is |
| --- | --- |
| `docs/*.md` | The chapters — this is what you edit |
| `docs/index.md` | Cover page and table of contents |
| `docs/_static/` | Images |
| `revisions.yaml` | The revision history (see below) |
| `docs/conf.py` | Build settings; rarely needs touching |
| `.vale.ini` | Style guide settings |

## Revisions

`revisions.yaml` is the only place a revision number is written. It fills in the
cover page, the revision table, the page footers, and the PDF filename —
so there is nowhere for it to drift out of step.

A revision being written is marked `draft: true`, and says so on the cover and
in the footer. Removing that line issues it, which requires an approver and an
effective date. **Check with the document owner before issuing a revision.**

Tagging a revision builds the PDF and attaches it to a GitHub release:

```sh
git tag v1.1 && git push --tags
```

---

Generated from [spiri-docs-tooling](https://github.com/spiri-robotics/spiri-docs-tooling).
