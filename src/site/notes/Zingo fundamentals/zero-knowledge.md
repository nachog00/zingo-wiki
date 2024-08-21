---
{"dg-publish":true,"permalink":"/zingo-fundamentals/zero-knowledge/","title":"Zero knowledge"}
---

## Zero Knowledge in Zcash: A Simple Explanation

Zero-knowledge proofs [[Zero-knowledge proofs\|Zero-knowledge proofs]] are a cryptographic technique that allows one party (the prover) to prove to another party (the verifier) that a statement is true, without revealing any information beyond the validity of the statement itself.  

In the context of [[Zcash\|Zcash]], zero-knowledge proofs are used to enable private transactions. When a user sends a Zcash transaction, the transaction details (sender, recipient, amount) are encrypted and included in the blockchain. However, the network still needs to verify that the transaction is valid (i.e., the sender has enough funds, the transaction doesn't create new coins out of thin air, etc.) without revealing the transaction details.

This is where zero-knowledge proofs come in. The sender constructs a zero-knowledge proof that demonstrates the validity of the transaction without revealing any of the private details. The network can verify this proof, ensuring the transaction is legitimate while preserving the privacy of the users involved.

**Key benefits of zero-knowledge in Zcash:**

- **Privacy:** Users can transact without revealing their financial information to the public or even to other network participants.
- **Security:** The network can verify transactions without compromising the privacy of the users.
- **Fungibility:** All Zcash coins are interchangeable, as there is no way to trace their transaction history.

**In essence, zero-knowledge in Zcash allows for private and secure transactions on a public blockchain, providing users with greater control over their financial information.**