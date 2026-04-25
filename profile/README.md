<div align="center">

<img src="https://github.com/DineroLabs.png?size=180" width="120" alt="Dinero" />

# Dinero — Real Money For Free People

**A post-quantum, utreexo-native, fair-launched cryptocurrency.**
Self-custody by default. No premine.

[![Latest release](https://img.shields.io/github/v/release/DineroLabs/dinero-releases?label=release)](https://github.com/DineroLabs/dinero-releases/releases/latest)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/DineroLabs/dinero-releases/blob/main/LICENSE)
[![Website](https://img.shields.io/badge/website-dinero--coin.com-0066CC)](https://dinero-coin.com)

</div>

---

## What makes Dinero different

| | |
|---|---|
| **Post-quantum native** | Coinbase outputs accept both Taproot (`din1p…`) and **P2MR** (`din1r…`), a hash-based signature scheme that survives Shor's algorithm. Every block can be spent today and decades from now. |
| **Utreexo from genesis** | The full UTXO set lives in a 1-KB accumulator commitment, not a 100-GB database. Light nodes verify the chain end-to-end without trusting anyone. |
| **128-byte block header** | Native `utreexo_root` field at offset `0x44`. No bolt-ons, no legacy compatibility cruft. |
| **Open mining stack** | Stratum V2 + Job Declaration over Noise NX lets miners own their coinbase outputs — no pool can redirect rewards. |
| **Fair launch** | No premine, no ICO, no insider allocation. Every coin in circulation was mined under the same rules every miner faces today. |

## Get started

### Run the wallet (macOS, signed + notarized)
👉 **[Download the latest release](https://github.com/DineroLabs/dinero-releases/releases/latest)**

Pick `Dinero-vX.Y.Z-macOS-arm64-qt.zip`, double-click after extracting. Apple Silicon only for now.

### Run a node
The signed `dinerod` daemon ships in every release bundle — extract `Dinero-vX.Y.Z-macOS-arm64.tar.gz` and launch:
```bash
./Dinero-vX.Y.Z-macOS-arm64/dinerod --datadir ~/.dinero
```
Daemon source access is currently limited to verified contributors — email `team@dinero-coin.com` if you need it.

### Get an address
Open the wallet, go to **Receive**, pick **Taproot** (`din1p…`) or **Quantum-Safe P2MR** (`din1r…`), click **New Address**.

## Repositories

| Repo | What it is |
|---|---|
| 🚀 **[dinero-releases](https://github.com/DineroLabs/dinero-releases)** | Signed binary releases (start here) |
| 🖥️ [dinero-qt](https://github.com/DineroLabs/dinero-qt) | Cross-platform desktop wallet |
| 📱 [DineroDPI](https://github.com/DineroLabs/DineroDPI) | iOS self-custody wallet. App Store builds exclude mining; developer builds may expose advanced tools. |
| 🌐 [dinero-explorer](https://github.com/DineroLabs/dinero-explorer) | Web block explorer |
| ⛏️ [dinero-sv2](https://github.com/DineroLabs/dinero-sv2) | Stratum V2 + Job Declaration (CPU + GPU miners) |
| 🔌 [dinero-stratum](https://github.com/DineroLabs/dinero-stratum) | Legacy Stratum V1 server (ASIC compatibility) |

> **Daemon source (`dinerod`) and the wDIN ↔ Base bridge server are kept private** while the chain stabilises. The signed binaries in [dinero-releases](https://github.com/DineroLabs/dinero-releases) are the trust anchor.

## Network

- **Mainnet RPC**: `20998` · **P2P**: `20999`
- **Reference SV2 pool**: `172.93.160.131:4444` (Noise pubkey: `17fc0efc6f937f3dd070b9d79da8b387f05a68598ecfd646db65735be5477f5f`)
- **Reference V1 stratum**: `127.0.0.1:3333` (run your own; user-launchable from the GUI)
- **Genesis**: `0000001c36abf27e2c233ff40ed0c08888926c24450f3bff82a047ae1528b76f` · 2026-04-17 00:00:00 UTC · nBits `0x1d31ffce` · 50× easier than Bitcoin floor

## Contribute

Pull requests welcome on any public repo. For coordination, security disclosures, or partnership inquiries see the individual repo `SECURITY.md` / `CONTRIBUTING.md`.

## Verifying releases

All `Dinero-Qt.app` bundles are signed with **Developer ID Application: Mirsad Hajdarevic (JXJS6ZA5FJ)** and notarized by Apple. Verify locally:

```bash
spctl -a -t exec -vv Dinero-Qt.app
# Expected: accepted, source=Notarized Developer ID
```

CLI binaries ship with `SHA256SUMS.txt` next to each archive.

## License

MIT. See [LICENSE](https://github.com/DineroLabs/dinero-releases/blob/main/LICENSE).

---

<div align="center">
<sub>Dinero · Real Money For Free People · <a href="https://dinero-coin.com">dinero-coin.com</a></sub>
</div>
