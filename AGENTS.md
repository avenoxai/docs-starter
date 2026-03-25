# AGENTS.md - Slinq Docs Repo

## Repo Role

This repository is the public Mintlify documentation site for Slinq.

- Docs repo path: `/Users/avenox/Desktop/Desktop/empire/slinqdocs`
- Product/codebase repo path: `/Users/avenox/Desktop/Zyper/slinq`

Do not confuse the two:

- The current working codebase for contracts, backend, and frontend lives in the separate `slinq` repo.
- This repo only contains the Mintlify content that powers the public docs site.

## Source of Truth

When updating contract or integration docs, prefer these sources in the codebase repo:

1. Mainnet registry: `/Users/avenox/Desktop/Zyper/slinq/artifacts/contracts/mainnet/contracts.json`
2. Verified contract interfaces under `/Users/avenox/Desktop/Zyper/slinq/contracts/src/interfaces/`
3. Hook and factory implementations when fee mechanics or launch behavior are discussed

For runtime address discovery, the public docs should point readers to:

- `GET https://slinq.meme/api/config/contracts`

## Writing Rules

- Public docs are for end users first. Keep product pages focused on what users see and do.
- Avoid exposing backend storage details, internal job flows, or unnecessary implementation plumbing in end-user pages.
- The `developers` tab can be more technical, but it should still prefer stable integration guidance over internal architecture trivia.
- Treat PancakeSwap Infinity / vNext as the current production stack unless a page is explicitly labeled historical or legacy.
- V3 contracts are actively used for V3 pools alongside the Infinity contracts.

## Consistency Rules

- Keep English and `zh-Hans` pages aligned when changing product mechanics.
- Keep fee mechanics consistent everywhere:
  - launch MEV window
  - fee caps
  - creator / initializer / protocol splits
- Prefer the docs repo for wording changes and the codebase repo for behavioral truth.
