# Keysingate schemas

Machine-readable schemas for the core documents. They are served from the
addresses that match the `$id` field inside each file:

| Document | Address |
|---|---|
| `common` | <https://schema.keysingate.com/core/v1/common.json> |
| `emission` | <https://schema.keysingate.com/core/v1/emission.json> |
| `allocation` | <https://schema.keysingate.com/core/v1/allocation.json> |
| `binding` | <https://schema.keysingate.com/core/v1/binding.json> |
| `receipt` | <https://schema.keysingate.com/core/v1/receipt.json> |
| `checkpoint` | <https://schema.keysingate.com/core/v1/checkpoint.json> |
| `closure` | <https://schema.keysingate.com/core/v1/closure.json> |

## Editing

**This repository is not edited.** It is built from the source by
`scripts/publish_schemas.py`; an edit made here will be overwritten by the next
build, and until then it will disagree with the implementation.

## What the schemas do not express

A schema constrains shape, not rules. Everything that requires comparing several
documents, or arithmetic, lies outside it: coverage of a block by its
allocations, uniqueness of a binding, the requirement for `prev_closure` from the
second block onward, time bounds, signatures.

**An implementation that has checked only the schema has not checked the
document.**

## Licence

Apache License 2.0 — see `LICENSE`.
