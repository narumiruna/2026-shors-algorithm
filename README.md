# 量子威脅與加密貨幣安全 — Shor 演算法深度解析

A single-page educational site (Traditional Chinese) that explains how Shor's algorithm and recent quantum-computing breakthroughs threaten the cryptographic foundations of Bitcoin, Ethereum, and other blockchains.

> **Context — 2026-03-31:** Google QuantumAI published a whitepaper showing the physical-qubit cost to break elliptic-curve cryptography is **20× lower** than previous estimates. On the same day, ArXiv paper [2603.28627](data/2603.28627v1.pdf) demonstrated that only ~26 000 neutral-atom qubits are required to crack ECC-256. Ethereum Foundation researcher Justin Drake responded publicly, raising his estimate of a pre-2032 "Q-Day" to 10 %.

---

## Contents

| Section | Topic |
|---------|-------|
| 0. 摘要總覽 | Executive summary and key statistics |
| 1. Justin Drake 的貼文 | Context from the Ethereum Foundation researcher |
| 2. 量子位元（Qubit） | Classical bits vs. qubits |
| 3. 疊加與糾纏 | Superposition and entanglement |
| 4. 量子閘 | Quantum gates and circuits |
| 5. 量子傅立葉轉換 | Quantum Fourier Transform (QFT) |
| 6. Shor 演算法概覽 | Algorithm overview and steps |
| 7. 階數求解問題 | Order-finding problem |
| 8. 數學原理 | Mathematical derivation |
| 9. 複雜度分析 | Complexity analysis |
| 10. RSA 加密 | RSA and integer factorisation |
| 11. 橢圓曲線密碼學 | ECC and the discrete-logarithm problem |
| 12. Bitcoin 的 ECDSA | Bitcoin signing and key exposure |
| 13. Google 白皮書 | Google QuantumAI 2026 whitepaper breakdown |
| 14. ArXiv 2603.28627 | Neutral-atom qubit route |
| 15. 兩篇論文比較 | Side-by-side comparison |
| 16. 威脅時間軸 | Threat timeline |
| 17. 後量子密碼學 | Post-quantum cryptography (PQC) |
| 18. 以太坊的因應策略 | Ethereum migration plan |
| 19. 休眠數位資產 | Dormant / P2PK Bitcoin at risk |
| 20. 參考資料 | References |

---

## Files

```
index.html          # All content and page structure
style.css           # Visual system, layout, responsive design
data/
  2603.28627v1.pdf              # ArXiv paper (neutral-atom route)
  cryptocurrency-whitepaper.pdf # Google QuantumAI 2026 whitepaper
```

---

## Local Development

No build pipeline is required. Serve the repo root with any static HTTP server:

```bash
# Python 3 (built-in)
python -m http.server 8000
# then open http://localhost:8000
```

Mathematical notation is rendered by [MathJax 3](https://www.mathjax.org/) loaded from the jsDelivr CDN — an internet connection is needed for that to work.

---

## Contributing

- Use **2-space indentation** in HTML and CSS files.
- Keep content and semantics in `index.html`; keep presentation in `style.css`.
- Use semantic, descriptive IDs and class names (e.g. `#sidebar`, `.stat-card`).
- Write scoped, imperative commit messages (e.g. `docs: clarify quantum timeline section`).
- PRs should include a description of the purpose, the changed files, and manual verification steps.