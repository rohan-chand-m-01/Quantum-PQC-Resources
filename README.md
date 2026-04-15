# Quantum Post-Quantum Cryptography (PQC) - Free Learning Resource

"The quantum computer that breaks RSA doesn't need to exist tomorrow - your encrypted traffic is being harvested today."

This repository is a curated, end-to-end, completely free learning path to master Quantum PQC from zero to research-grade.

---

## Navigation

- [01 Math Foundations](./01_Math_Foundations)
- [02 Classical Cryptography](./02_Classical_Cryptography)
- [03 Quantum Threat Model](./03_Quantum_Threat_Model)
- [04 PQC Algorithms](./04_PQC_Algorithms)
- [05 Implementation And Coding](./05_Implementation_And_Coding)
- [06 Research Frontier](./06_Research_Frontier)
- [07 Videos And Lectures](./07_Videos_And_Lectures)

---

## Why Quantum PQC is the Most Urgent Security Problem of Our Decade

### The Core Threat
Current public-key cryptography (RSA, ECC, Diffie-Hellman) relies on the computational difficulty of:
- Factoring large integers - broken by Shor's Algorithm on a quantum computer
- Discrete logarithm problem - also broken by Shor's Algorithm

A Cryptographically Relevant Quantum Computer (CRQC) - estimated to arrive within 5-15 years - will render today's internet security infrastructure obsolete overnight.

### "Harvest Now, Decrypt Later" (HNDL)
Nation-state actors are actively collecting encrypted traffic today with the intent to decrypt it once a CRQC becomes available.
- Your TLS traffic from 2024 could be decrypted in 2033.
- Long-lived secrets (medical records, state secrets, financial data) are already compromised in transit.
- The migration window is NOW.

### The NIST Milestone (August 2024)
NIST finalized the first PQC standards after an 8-year global competition:

| Standard | Algorithm | Purpose | Based On |
|---|---|---|---|
| FIPS 203 | ML-KEM (Kyber) | General encryption / KEM | Module Lattices |
| FIPS 204 | ML-DSA (Dilithium) | Digital signatures | Module Lattices |
| FIPS 205 | SLH-DSA (SPHINCS+) | Digital signatures | Hash functions |
| FIPS 206 | FN-DSA (Falcon) | Digital signatures | NTRU Lattices |

---

## The Top 1% Learning Roadmap

```
Phase 1: Math Foundations (2-3 weeks)
    |
Phase 2: Classical Cryptography (2-3 weeks)
    |
Phase 3: Quantum Computing Threat Model (1-2 weeks)
    |
Phase 4: PQC Algorithms - Deep Dive (4-6 weeks)
    |
Phase 5a: Implementation & Coding       Phase 5b: Research Frontier
```

---

## Phase 1 - Mathematical Foundations

Lattices, rings, and module algebra are the bedrock.

| Book | Link | What You Learn |
|---|---|---|
| Introduction to Mathematical Cryptography | [PDF](https://link.springer.com/book/10.1007/978-1-4939-1711-2) | Number theory, elliptic curves, lattices |
| A Course in Number Theory and Cryptography | [Free PDF](https://link.springer.com/book/10.1007/978-1-4419-8592-7) | Deep number theory foundations |
| Linear Algebra Done Right | [Free online](https://linear.axler.net/) | Linear algebra for lattice math |
| Lattice-Based Cryptography (Short Intro) | [Free PDF](https://cims.nyu.edu/~regev/papers/pqc.pdf) | The key math connection to PQC |

---

## Phase 4 - YouTube Channels & Video Lectures

### Channels You Must Subscribe To

| Channel | Link | What They Cover |
|---|---|---|
| Christof Paar | [YouTube Playlist](https://www.youtube.com/channel/UC1usFRN4LCMcfIV7UjHNuQg) | Best classical to PQC bridge |
| Dan Boneh (Stanford) | [YouTube](https://www.youtube.com/results?search_query=dan+boneh+cryptography+stanford) | World-class crypto theory |
| IACR | [YouTube](https://www.youtube.com/c/TheIACR) | All top crypto research talks |
| Qiskit (IBM Quantum) | [YouTube](https://www.youtube.com/c/qiskit) | Quantum algorithms in depth |

---

## Bonus: Free Courses & Online Resources

| Resource | Link | Level |
|---|---|---|
| Dan Boneh Cryptography I | [Free Audit](https://www.coursera.org/learn/crypto) | Beginner to Intermediate |
| MIT 6.875: Cryptography | [MIT OCW](https://ocw.mit.edu/courses/6-875-cryptography-spring-2005/) | Advanced |
| Cryptopals Challenges | [cryptopals.com](https://cryptopals.com) | Hands-on coding |
| CryptoHack | [cryptohack.org](https://cryptohack.org) | CTF-style learning |

---

## Recommended Study Schedule (Top 1% Pace)

| Week | Focus | Daily Time |
|---|---|---|
| 1-2 | Linear algebra, modular arithmetic, groups/rings | 2-3 hrs |
| 3-4 | Classical crypto: RSA, ECC, AES | 2-3 hrs |
| 5 | Quantum computing basics, Shor's Algorithm | 2-3 hrs |
| 6-7 | Lattice math: LWE, SVP, NTRU | 3-4 hrs |
| 8-9 | ML-KEM deep dive - FIPS 203 + Kyber paper | 3-4 hrs |
| 10-11 | ML-DSA + SLH-DSA - FIPS 204 + 205 | 3-4 hrs |
| 13-14 | Hands-on: liboqs, PQClean, implement key exchange | 3-4 hrs |
| 17+ | Research papers, IACR talks, contribute to OQS | Ongoing |

---

## Quick Reference Links

- NIST FIPS 203 (ML-KEM): [Link](https://doi.org/10.6028/NIST.FIPS.203)
- NIST FIPS 204 (ML-DSA): [Link](https://doi.org/10.6028/NIST.FIPS.204)
- NIST FIPS 205 (SLH-DSA): [Link](https://doi.org/10.6028/NIST.FIPS.205)
- Open Quantum Safe (liboqs): [GitHub](https://github.com/open-quantum-safe/liboqs)
- IACR ePrint Archive: [Link](https://eprint.iacr.org)

---

## Migration Checklist (For Practitioners)

- [ ] Inventory all systems using RSA, ECDH, ECDSA, DH
- [ ] Identify data with long-term sensitivity (stop HNDL exposure)
- [ ] Plan hybrid deployment (classical + PQC simultaneously)
- [ ] Test ML-KEM key exchange in your TLS stack
- [ ] Update certificate infrastructure for ML-DSA
- [ ] Follow NIST IR 8547 transition timeline

## Contributors
- Venkatesh Reddy
- Krish Kumar Sharma
- Claude

---

## License
CC0 - Free for all use. Maintained by the contributors listed above.

Repository: [Quantum-PQC-Resources-](https://github.com/rohan-chand-m-01/Quantum-PQC-Resources-)
