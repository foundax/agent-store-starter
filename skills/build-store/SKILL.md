---
name: build-store
description: Build a complete online store (pages, products, shipping, returns, promotions, legal pages) with a local preview and simulated checkout, starting from a Foundax reference design. Use when the user asks to build an online store, shop or e-commerce site.
---

# Build an online store

1. Choose a reference with the user. `hush` is a lighting store built around an interactive lit photograph.
   `strata` is a keyboard store built around a CSS 3D model that separates into layers and plays switch sounds.
   If the user names neither, briefly describe both and let them choose.
2. In an empty folder, run `npx foundax@latest init --showcase <reference>`. It creates a new folder and prints
   its path.
3. Read `AGENTS.md` in that folder and follow its workflow from the first step. It tells you which facts to ask
   the user for. Never invent prices, policies or legal terms.
4. Finish with `npx foundax@latest check` passing and the store open in `npx foundax@latest preview`.
   Report what you inspected in the preview and what remains unverified.
5. The preview is local only, with payments and delivery simulated. When the user wants to import, use the
   authorization saved by their Foundax prompt. If this is a public `--showcase` build, ask them to sign in at
   https://foundax.com, choose a target workspace in the reference's prompt dialog and authorize access. Run
   `npx foundax@latest connect --origin https://foundax.com --code=THE_AUTHORIZATION` in the completed folder.
6. Run `npx foundax@latest import --check`, repair reported source/data problems, then run `npx foundax@latest import`.
   Repeat fixes and imports yourself within the authorized project. After a timeout, query `npx foundax@latest status`
   before retrying. Keep the authorization file out of Git, source and packages. It lasts 7 days and can be revoked
   in Settings → Security → Agent authorizations. Expired access, missing permissions, storage or subscription
   requirements need the user's action; never purchase capacity or a plan without their instruction.
7. Return the website editor address and explain remaining launch steps. Import changes real business data;
   publishing is separate and requires publication entitlement and available site quota. Have the user configure
   payments and domains, complete readiness checks and publish in Foundax. Manual zip import remains available
   with `npx foundax@latest pack`.

