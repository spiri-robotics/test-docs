# Revision history

This table is generated from `revisions.yaml` at the root of this repository.
Do not edit it here -- add an entry there and it appears below, on the cover
page, and in the PDF footer.

```{revision-history}
```

## Issuing a revision

1. Add an entry to the bottom of `revisions.yaml`.
1. Fill in `approver` and `effective_date`. The build fails without them.
1. Commit, then tag: `git tag v<revision> && git push --tags`.
1. CI builds the PDF and attaches it to a GitHub release. That release asset is
   the controlled copy -- link people to it rather than to the Read the Docs
   PDF, which is rebuilt in place and can change under them.

