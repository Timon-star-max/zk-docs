---
title: "Technical Description"
summary: "We tried to make a simple but well-structured theme. Managing the content is straightforward but still comes with some helpful features."
eleventyNavigation:
  key: Technical Description
  parent: Getting Started
  order: 2
---

Public Key Registries: The public registry where ephemeral public keys are published allows participants (like receivers) to scan and identify stealth addresses. This mechanism helps maintain privacy without revealing the actual recipient’s address.

- Zkml Protocol implements stealth addresses on the XRP EVM compatible chain using a combination of cryptographic techniques to ensure transaction security and user privacy. Let’s break down the key steps and encryption methods involved:

- Stealth Addresses Generation: The receiver generates a root spending key (receiver private key) and computes a stealth meta-address (receiver public key or receiver’s address) using elliptic curve cryptography. This stealth meta-address (receiver’s address) becomes a publicly known identifier for the receiver on the blockchain.

- Stealth Addresses Generation: The receiver generates a root spending key (receiver private key) and computes a stealth meta-address (receiver public key or receiver’s address) using elliptic curve cryptography. This stealth meta-address (receiver’s address) becomes a publicly known identifier for the receiver on the blockchain.

- Shared Secret Creation: The Sender combines his ephemeral key (sender’s private key) with the Receiver’s stealth meta-address (receiver's public key) to create a shared secret (S). This shared secret is a private connection between the Sender and Receiver.

- Ephemeral Public Key Publishing: The sender creates an ephemeral public key (sender public key) from his ephemeral key (sender private key) and publishes it on a public registry. This public key can be seen by anyone.

- Transaction Process: The sender sends funds to a stealth address, which is derived from the combination of his ephemeral key (sender's private key) and the Receiver’s meta-address (receiver's public key).

- Recipient’s Discovery: The receiver scans the public registry for ephemeral public keys (sender public key) and tries to unlock special addresses (stealth addresses) using his spending key (receiver private key) and the shared secrets (S). If funds are found in an address, the Receiver can access them.

- Address Ownership and Privacy: The transaction details are recorded on the blockchain, but the connection between the recipient’s real address and the stealth address remains private. This adds a layer of privacy by making it difficult for external observers to link transactions to specific recipients.

- The cryptographic techniques used in this process include:

   Elliptic Curve Cryptography (ECC): This is used to generate private and public keys, compute shared secrets, and create addresses. ECC provides a secure way to perform mathematical operations that ensure transaction security and privacy.

   Hash Functions: Hashing is used to derive addresses from public keys and shared secrets. Hash functions are one-way functions that add an extra layer of security to the process.

   Public Key Registries: The public registry where ephemeral public keys are published allows participants (like receivers) to scan and identify stealth addresses. This mechanism helps maintain privacy without revealing the actual recipient’s address.