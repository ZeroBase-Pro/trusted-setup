# Powers of Tau Public Parameters (BN254)

This repository contains the **Powers of Tau public parameters** generated over the **BN254 curve**.  

The parameters were produced through a large-scale multi-party Trusted Setup ceremony organized by **ZEROBASE**, recognized as the **largest Trusted Setup ceremony ever held**, with a record-breaking **37,209** contributions worldwide.  

These files are the output of **Groth16 Phase 1 (Powers of Tau)**, but they are **general-purpose** and can be reused across multiple zero-knowledge proof systems and polynomial commitment schemes.

---

## 📖 Background

Zero-knowledge proof systems often require a **Structured Reference String (SRS)** as part of their cryptographic setup.  
The first stage — the **Powers of Tau (Phase 1)** — produces universal parameters that can be reused across circuits and protocols.  

**Key properties:**
- ✅ **Circuit-independent**: not bound to any specific application  
- ✅ **Reusable**: one ceremony can serve many protocols  
- ✅ **Secure**: as long as one participant is honest, the resulting parameters are trustworthy  

---

## 🌍 The ZEROBASE Guinness Challenge

ZEROBASE launched a groundbreaking initiative aiming to set a Guinness World Record:  
**"Most contributions to a trusted setup for a Zero-Knowledge Proof (ZKP) in a 3-month timeframe."**

Through this global challenge, we achieved two major goals:

1. **Provide a strong foundation for gnark**: establishing a universal trusted setup that becomes a core component for future gnark circuit development.  
2. **Promote ZKP technology worldwide**: demonstrating the collective power of the cryptography community and raising awareness of privacy-preserving technologies.  

### Why more participants matter

- **Multi-party contributions**: the more independent participants, the lower the risk of a single point of failure.  
- **Toxic waste disposal**: intermediate secret values generated during the process must be discarded; if even one participant discards their secret, the system is secure.  
- **Security guarantee**: with **37,209 contributions**, the probability that *all* participants were dishonest is negligible — more contributors directly translate to stronger security and trust.  

Trusted setup ceremonies are critical in blockchain and privacy-preserving technologies. For example, Ethereum relied on trusted setups when deploying scalability mechanisms. ZEROBASE’s record-breaking ceremony set a new standard for openness, inclusivity, and verifiable cryptographic foundations.

---

## 🔄 General Applicability

Although these parameters originated from **Groth16 Phase 1**, they are **not limited to Groth16**. They can be reused in multiple protocols, including but not limited to:

- **gnark** (Go ecosystem, Phase 2 setup for circuit-specific proving/verifying keys)  
- **Groth16** (circom/snarkjs workflow)  
- **PLONK** (requires powers of tau as its universal SRS)  
- **KZG Polynomial Commitments** (powers of tau form the foundation of the scheme)  
- **Other polynomial IOP-based protocols** (e.g., Marlin, Sonic, Halo2)  

---

## 📂 Files

- `bn254_pow22.ptau`  
  - Public parameter file, where `pow22` supports up to \(2^{22}\) constraints.  
- `checksums.txt`  
  - Contains SHA256 hashes for integrity verification.  

---

## ✅ Verification

```bash
sha256sum bn254_pow22.ptau

