# Quantum Post-Quantum Cryptography (PQC) - Top 1% Free Learning Resource

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

### "Harvest Now, Decrypt Later" (HNDL) - Why This Is Already Happening
Nation-state actors are actively collecting encrypted traffic today with the intent to decrypt it once a CRQC becomes available. This means:
- Your TLS traffic from 2024 could be decrypted in 2033
- Long-lived secrets (medical records, state secrets, IP, financial data) are already compromised in transit
- The migration window is NOW, not when quantum computers arrive

### The NIST Milestone (August 2024)
After an 8-year, 82-algorithm global competition, NIST finalized the first PQC standards:

| Standard | Algorithm | Purpose | Based On |
|---|---|---|---|
| FIPS 203 | ML-KEM (Kyber) | General encryption / Key encapsulation | Module Lattices |
| FIPS 204 | ML-DSA (Dilithium) | Digital signatures | Module Lattices |
| FIPS 205 | SLH-DSA (SPHINCS+) | Digital signatures | Hash functions |
| FIPS 206 | FN-DSA (Falcon) | Digital signatures | NTRU Lattices |

Federal agencies are mandated to begin migration. IETF is incorporating ML-KEM into TLS. Cloudflare already protects 16%+ of requests with PQC.

### Who Needs PQC Right Now
- Governments & Defense agencies
- Banks, stock exchanges, payment systems
- Healthcare systems storing long-term patient data
- Certificate Authorities & PKI infrastructure
- Cloud providers, IoT devices, VPNs
- Blockchain & Digital ID systems

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

Lattices, rings, and module algebra are the bedrock of PQC.

### Free Textbooks

| Book | Link | What You Learn |
|---|---|---|
| Introduction to Mathematical Cryptography - Hoffstein, Pipher, Silverman | [PDF (Springer)](https://link.springer.com/book/10.1007/978-1-4939-1711-2) | Number theory, elliptic curves, lattices |
| A Course in Number Theory and Cryptography - Neal Koblitz | [Free PDF](https://link.springer.com/book/10.1007/978-1-4419-8592-7) | Deep number theory foundations |
| Linear Algebra Done Right - Axler | [Free online](https://linear.axler.net/) | Linear algebra for lattice math |
| Abstract Algebra - Dummit & Foote excerpts | [MIT OCW 18.703](https://ocw.mit.edu/courses/18-703-modern-algebra-spring-2013/) | Group/ring theory for lattice cryptography |
| Lattice-Based Cryptography (Short Intro) - Micciancio & Regev | [Free PDF](https://cims.nyu.edu/~regev/papers/pqc.pdf) | The key math connection to PQC |

### Key Topics to Master
- Modular arithmetic, groups, rings, fields
- Linear algebra over integer rings
- Probability and information theory basics
- Lattices: Shortest Vector Problem (SVP), Closest Vector Problem (CVP)

---

## Phase 2 - Classical Cryptography Foundations

Understand what we're replacing and why it breaks.

### Free Textbooks

| Book | Link | What You Learn |
|---|---|---|
| Serious Cryptography - Jean-Philippe Aumasson | [Free Chapter Previews](https://nostarch.com/seriouscrypto) | Modern practical crypto (RSA, ECC, AES, hashing) |
| Applied Cryptography - Bruce Schneier | [Free online](https://www.schneier.com/books/applied-cryptography/) | Comprehensive classical crypto reference |
| Cryptography: Theory and Practice - Stinson & Paterson | [Springer Free Access](https://link.springer.com/book/10.1201/9781315282497) | Theoretical foundations |
| Dan Boneh's Cryptography I (Stanford) | [Coursera - Free Audit](https://www.coursera.org/learn/crypto) | Best online crypto course on the planet |
| An Introduction to Mathematical Cryptography | [Springer Free PDF](https://link.springer.com/book/10.1007/978-1-4939-1711-2) | Math-first approach |

### Key Concepts
- RSA: why factoring is hard classically
- ECC: discrete log on elliptic curves
- Diffie-Hellman key exchange
- Digital signatures: DSA, ECDSA
- Why Shor's algorithm destroys all of the above

---

## Phase 3 - Quantum Computing & The Threat Model

Understand what quantum computers do to cryptography.

### Free Textbooks & Lecture Notes

| Resource | Link | What You Learn |
|---|---|---|
| Quantum Computation and Quantum Information - Nielsen & Chuang | [Cambridge (Free Chapter Access)](https://www.cambridge.org/9781107002173) | The bible of quantum computing |
| Quantum Computing: An Applied Approach - Hidary | [Supplementary Materials](https://github.com/jackhidary/quantumcomputingbook) | Practical QC with code |
| Lecture Notes on Quantum Algorithms - Andrew Childs | [Free PDF (UMD)](https://www.cs.umd.edu/~amchilds/qa/qa.pdf) | Shor's, Grover's algorithms - deep formal treatment |
| Quantum Computing Since Democritus - Scott Aaronson | [Free Lecture Notes](https://www.scottaaronson.com/democritus/) | Intuitive explanation of QC |
| Introduction to Quantum Information Science - Wilde | [Free arXiv PDF](https://arxiv.org/abs/1106.1445) | Information-theoretic view |

### Key Concepts
- Qubits, superposition, entanglement
- Quantum gates, quantum circuits
- Shor's Algorithm - why it breaks RSA/ECC
- Grover's Algorithm - why it halves symmetric key security
- Quantum Resource Estimates for breaking algorithms

---

## Phase 4 - Post-Quantum Cryptography Algorithms

Four major families of PQC:

1. **Lattice-Based**: Most practical, NIST winners (ML-KEM, ML-DSA).
2. **Hash-Based**: Oldest, most conservative (SLH-DSA).
3. **Code-Based**: Mature foundations (McEliece).
4. **Isogeny-Based**: Significant research history (SIKE - now deprecated).

### Comprehensive References

| Book / Paper | Link | What You Learn |
|---|---|---|
| Introduction to Post-Quantum Cryptography - Bernstein & Lange | [Free PDF](https://pqcrypto.org/www.springer.com/cda/content/document/cda_downloaddocument/9783540887010-c1.pdf) | The original comprehensive PQC overview |
| A Decade of Lattice Cryptography - Peikert | [Free PDF](https://eprint.iacr.org/2015/939.pdf) | Deep lattice crypto foundations |
| Learning With Errors - Regev's Original Paper | [Free PDF](https://cims.nyu.edu/~regev/papers/qcrypto.pdf) | The math foundation of Kyber/Dilithium |
| CRYSTALS-Kyber Spec (ML-KEM) | [Official NIST FIPS 203](https://doi.org/10.6028/NIST.FIPS.203) | The actual standard |
| CRYSTALS-Dilithium Spec (ML-DSA) | [Official NIST FIPS 204](https://doi.org/10.6028/NIST.FIPS.204) | The actual standard |
| SPHINCS+ Spec (SLH-DSA) | [Official NIST FIPS 205](https://doi.org/10.6028/NIST.FIPS.205) | The actual standard |
| Falcon (FN-DSA) Specification | [Official Website](https://falcon-sign.info/falcon.pdf) | NTRU lattice signatures |

---

## Phase 5a - Implementation & Hands-On Coding

### Open Source Libraries

| Library | Language | Link | Description |
|---|---|---|---|
| liboqs (Open Quantum Safe) | C / Python / Go | [GitHub](https://github.com/open-quantum-safe/liboqs) | Reference PQC implementation library |
| OQS-OpenSSL | C | [GitHub](https://github.com/open-quantum-safe/openssl) | PQC-enabled fork of OpenSSL |
| PQClean | C | [GitHub](https://github.com/PQClean/PQClean) | Clean implementations of NIST candidates |
| CRYSTALS-Kyber Reference | C | [GitHub](https://github.com/pq-crystals/kyber) | Official Kyber/ML-KEM reference |
| Bouncy Castle PQC | Java | [GitHub](https://github.com/bcgit/bc-java) | Production-ready Java implementation |

### Projects to Build
1. Implement ML-KEM key exchange using liboqs.
2. Build a PQC-secured TLS connection with OQS-OpenSSL.
3. Compare performance: RSA-2048 vs ML-KEM-768.
4. Implement a simple LWE-based encryption scheme from scratch.

---

## Phase 5b - Research Frontier

### Key Research Papers (via IACR ePrint)

- **On Lattices, Learning with Errors...** - Regev (2005) [Link](https://eprint.iacr.org/2005/449.pdf)
- **Crystals-Kyber: A CCA-Secure...** - Avanzi et al. [Link](https://eprint.iacr.org/2017/634.pdf)
- **Breaking SIDH/SIKE** - Castryck & Decru (2022) [Link](https://eprint.iacr.org/2022/975.pdf)
- **Quantum Resource Estimates...** - Roetteler et al. [Link](https://eprint.iacr.org/2017/598.pdf)

---

## Migration Checklist

- [ ] Inventory all systems using RSA, ECDH, ECDSA, DH
- [ ] Identify data with long-term sensitivity (stop HNDL exposure)
- [ ] Plan hybrid deployment (classical + PQC simultaneously)
- [ ] Test ML-KEM key exchange in your TLS stack
- [ ] Update certificate infrastructure for ML-DSA
- [ ] Monitor IETF drafts for protocol-specific guidance

---

## License
CC0 - Free for all use. Maintained by the community.

Repository: [Quantum-PQC-Resources-](https://github.com/rohan-chand-m-01/Quantum-PQC-Resources-)
