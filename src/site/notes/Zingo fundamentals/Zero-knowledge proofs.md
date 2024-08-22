---
{"dg-publish":true,"permalink":"/zingo-fundamentals/zero-knowledge-proofs/","title":"Zero-knowledge proofs"}
---

Zero-knowledge proofs, at their core, are a fascinating intersection of mathematics and cryptography. They enable the prover to convince the verifier of the truth of a statement, without revealing any information beyond the fact that the statement is indeed true. Let's delve into the mathematical underpinnings of this powerful concept.

## **Formal Definition**

A zero-knowledge proof system for a language L consists of two probabilistic polynomial-time algorithms: a prover P and a verifier V. Given an input x, the prover aims to convince the verifier that x∈L without revealing any additional information.

The proof system must satisfy three properties:

1. **Completeness:** If x∈L, an honest prover can convince an honest verifier with high probability.
    
2. **Soundness:** If x∈/L, no cheating prover can convince an honest verifier with more than a negligible probability.
    
3. **Zero-knowledge:** For every (possibly malicious) verifier V∗, there exists a simulator S such that for any x∈L, the interaction between P and V∗ is computationally indistinguishable from the output of S on input x.
    

## **Mathematical Intuition**

The zero-knowledge property can be intuitively understood through the concept of a simulator. The simulator, without knowing the witness (the secret information that proves x∈L), can generate a transcript of the interaction between the prover and the verifier that is indistinguishable from a real interaction. This means that the verifier learns nothing from the interaction beyond the fact that x∈L.

## **Example: The Graph Isomorphism Problem**

Let's consider the graph isomorphism problem: given two graphs G1​ and G2​, determine if they are isomorphic (i.e., if there exists a bijection between their vertices that preserves adjacency).

A zero-knowledge proof for this problem could proceed as follows:

1. **Commitment:** The prover randomly permutes the vertices of G1​ to create a new graph H and sends a commitment (e.g., a cryptographic hash) of H to the verifier.
    
2. **Challenge:** The verifier randomly chooses one of the original graphs (say, G1​) and asks the prover to provide an isomorphism between H and the chosen graph.
    
3. **Response:** The prover provides the isomorphism. If the verifier chose G1​, the prover provides the original permutation used to create H. If the verifier chose G2​, and G1​ and G2​ are indeed isomorphic, the prover can compute an isomorphism between H and G2​ and provide that.
    
4. **Verification:** The verifier checks if the provided isomorphism is valid.
    

This process is repeated multiple times to increase the verifier's confidence. If the prover is honest, they can always provide a valid isomorphism. However, if the graphs are not isomorphic, a cheating prover will be caught with high probability.

## **Zcash and zk-SNARKs**

In Zcash, the specific type of zero-knowledge proof used is called a zk-SNARK. zk-SNARKs are particularly useful in the context of blockchains because they are:

- **Succinct:** The proofs are short and can be verified quickly.
- **Non-interactive:** The prover and verifier do not need to interact multiple times.
- **Argument of Knowledge:** The proof demonstrates that the prover knows the witness (the secret information).

These properties make zk-SNARKs ideal for ensuring the privacy and security of transactions on the Zcash blockchain.

## **In Conclusion**

Zero-knowledge proofs are a remarkable cryptographic tool that enables us to prove the validity of statements without revealing any unnecessary information. They play a crucial role in preserving privacy and security in Zcash and other blockchain applications. The mathematical foundations of zero-knowledge proofs are deep and fascinating, offering a glimpse into the power of cryptography to protect information in the digital age.

## Learning Resources
+ [Zero Knowledge What? An Introduction to Zero Knowledge](https://codethechange.stanford.edu/guides/guide_zk.html)