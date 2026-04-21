<div align="center">

<br>

<table border="0" cellspacing="0" cellpadding="0">
<tr>
<td align="center" style="background:#000000; padding: 40px 60px; border-left: 4px solid #ff5347; border-right: 4px solid #ff5347;">

<code style="color:#ff5347; font-size:11px; letter-spacing:4px;">▸▸ NIST POST-QUANTUM STANDARD ◂◂</code>

<h1 style="color:#fafafa; font-family:monospace; font-size:2.5em; letter-spacing:0.5em; margin: 10px 0;">
BENCHMARKING<br>POST-QUANTUM<br>CRYPTOGRAPHY
</h1>

<code style="color:#ff8a80; font-size:11px; letter-spacing:3px;">ML-KEM · ML-DSA · SLH-DSA</code>

</td>
</tr>
</table>

<br>

![Python](https://img.shields.io/badge/Python-3.x-ff5347?style=flat-square&logo=python&logoColor=white)
![NIST](https://img.shields.io/badge/NIST-Post--Quantum-000000?style=flat-square&logoColor=white&labelColor=ff5347)
![liboqs](https://img.shields.io/badge/liboqs-0.15.0-ff8a80?style=flat-square)
![Status](https://img.shields.io/badge/Status-Research-333?style=flat-square)

<br>

*Michał Kowalski · Dorian Gabler · Jan Jankowski*

<br>

</div>

---

## `> OVERVIEW`

This project benchmarks three **NIST-standardized post-quantum cryptographic algorithms**, measuring performance across key generation, encapsulation/signing, and decapsulation/verification.

> Quantum computers threaten the cryptographic foundations of modern security. This work evaluates the practical performance cost of transitioning to quantum-resistant alternatives.

---

## `> ALGORITHMS`

<div align="center">

| | Algorithm | Type | Standard |
|--|-----------|------|----------|
| 🔴 | **ML-KEM** | Key Encapsulation Mechanism | FIPS 203 |
| 🔴 | **ML-DSA** | Digital Signature | FIPS 204 |
| 🔴 | **SLH-DSA** | Hash-Based Digital Signature | FIPS 205 |

</div>

**ML-KEM** — Module-Lattice Key Encapsulation. Successor to Kyber. Replaces RSA and ECDH in key establishment protocols.

**ML-DSA** — Module-Lattice Digital Signature. Successor to Dilithium. Lattice-based signatures optimized for highly efficient performance.

**SLH-DSA** — Stateless Hash-Based Signature. Successor to SPHINCS+. Conservative construction grounded in symmetric primitives.

---

## `> GETTING STARTED`

**1. Build and install liboqs**
```bash
git clone --depth=1 https://github.com/open-quantum-safe/liboqs
cmake -S liboqs -B liboqs/build -DBUILD_SHARED_LIBS=ON
cmake --build liboqs/build --parallel 4
cmake --build liboqs/build --target install
```

**2. Clone and set up**
```bash
git clone https://github.com/<your-repo>/Benchmarking_Post-Quantum_Cryptographic_Algorithms
cd Benchmarking_Post-Quantum_Cryptographic_Algorithms

python -m venv .venv
.venv\Scripts\activate        # Windows
source .venv/bin/activate     # Linux / macOS

pip install -r requirements.txt
```

---

## `> STRUCTURE`

```
Benchmarking_Post-Quantum_Cryptographic_Algorithms/
│
├── ML-KEM/          # Key encapsulation benchmarks
├── ML-DSA/          # Digital signature benchmarks
├── SLH-DSA/         # Hash-based signature benchmarks
│
├── results/         # Output data & plots
├── requirements.txt
└── README.md
```

---

## `> BENCHMARKS`

Each algorithm is evaluated across:

- **Key Generation** — keypair generation time
- **Encapsulation / Signing** — time to encapsulate or sign
- **Decapsulation / Verification** — time to decapsulate or verify
- **Size Metrics** — key sizes, ciphertext and signature sizes

---

## `> REFERENCES`

- [NIST FIPS 203 — ML-KEM](https://csrc.nist.gov/pubs/fips/203/final)
- [NIST FIPS 204 — ML-DSA](https://csrc.nist.gov/pubs/fips/204/final)
- [NIST FIPS 205 — SLH-DSA](https://csrc.nist.gov/pubs/fips/205/final)
- [Open Quantum Safe — liboqs](https://github.com/open-quantum-safe/liboqs)

---

<div align="center">
<br>
<code>Michał Kowalski · Dorian Gabler · Jan Jankowski</code>
<br><br>
</div>
