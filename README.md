# Hi,

iOS engineer / builder. I make **open-source tools that help agentic / AI-assisted development ship quality deliverables**, guardrails that keep codebases sound when humans *and* AI agents write the code.

## 🚧 Current projects

### 🪨 [solid-like-a-rock](https://github.com/nenadvulic/solid-like-a-rock)
Architecture **and security** linter for Swift, built on [SwiftSyntax](https://github.com/swiftlang/swift-syntax) (real syntax trees, no fragile regex). A CI-ready guardrail for AI-assisted development: dependencies must point inward, insecure patterns must not ship — and the build fails when either rule breaks.

- 🔍 `init` command generates a starter config from your project's **real inter-module import graph** — deterministic, no LLM
- 🔐 **14 security rules** (Keychain misuse, hardcoded secrets, weak crypto, trust-all TLS, PII in logs, …) — calibrated on real codebases, [documented rule by rule](https://github.com/nenadvulic/solid-like-a-rock/blob/main/docs/security-rules.md), and usable **standalone** with `init --security`: no architecture config required
- 🐙 [GitHub Action](https://github.com/nenadvulic/solid-like-a-rock-action) for one-line CI integration
- 🍺 [Homebrew tap](https://github.com/nenadvulic/homebrew-solid-like-a-rock) for easy install

**Contributions are very welcome** — issues, ideas, PRs: see [CONTRIBUTING.md](https://github.com/nenadvulic/solid-like-a-rock/blob/main/CONTRIBUTING.md).

### 🪵 [deadwood](https://github.com/nenadvulic/deadwood) · _early WIP_
An agent-native dead-code guardrail for Swift, built **on top of** [Periphery](https://github.com/peripheryapp/periphery). It runs Periphery, then reports only the unused code a change *introduces* — scoped to your git diff — so reviews (and AI agents) see what *this* PR made dead, not a wall of pre-existing debt.

- 🎯 Diff-scoped: keeps only findings located in the lines your change touched
- 🚦 CI gate: exits non-zero only on newly-introduced dead code (`--no-fail` to opt out)
- 🧱 Early MVP — the diff-scoped engine; an agent hook, PR inline comments and assisted removal are next

### 🪪 [SerbianEIDKit](https://github.com/nenadvulic/SerbianEIDKit)
Swift package to read the **Serbian electronic ID card (lična karta)** on iOS & macOS over a CCID reader, built on Apple's **CryptoTokenKit** (`TKSmartCard`). Protocol reconstructed from the official app and validated on real cards.

- 📇 Reads the document, personal and residence files **+ the cardholder photo** (JPEG)
- 🧩 Pure Swift, zero dependencies; async/await API with an APDU-level log hook
- 🧪 Unit-tested little-endian TLV parser, plus a sample SwiftUI app

### 🚗 [SerbianVehicleKit](https://github.com/nenadvulic/SerbianVehicleKit)
Swift package to read the **Serbian vehicle registration card (saobraćajna dozvola)** on iOS & macOS over a CCID reader (**CryptoTokenKit**). Validated on real cards.

- 🧩 Nested **BER-TLV** parser (ISO 7816-4) + 3-variant applet selection
- 🚘 Extracts ~37 fields (vehicle, technical, owner/user), `Codable` for JSON
- 🙏 Vehicle protocol ported from [bas-celik](https://github.com/ubavic/bas-celik) (MIT)

## 🌱 Contributing to Swift open source

I've started contributing across the Swift ecosystem:

- [swiftlang/swift-syntax](https://github.com/swiftlang/swift-syntax)
- [swiftlang/swift-subprocess](https://github.com/swiftlang/swift-subprocess)
- [onevcat/Kingfisher](https://github.com/onevcat/Kingfisher)
- [danger/swift](https://github.com/danger/swift)

## 🤝 Contributions welcome

All contributions are welcome on my projects — bug reports, feature ideas, docs, code. If you're getting started with open source, I'm happy to help you land a first PR.

## 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-nenadvulic-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nenadvulic/)
