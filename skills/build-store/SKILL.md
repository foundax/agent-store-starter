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
5. Tell the user that the preview is local only, with payments and delivery simulated. To go live, they run
   `npx foundax@latest pack` and import the zip from the site list at https://foundax.com, which requires an account.
