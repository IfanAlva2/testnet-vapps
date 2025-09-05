# vApp Submission: zkThrottle

## Verification
```yaml
github_username: "IfanAlva2"
discord_id: "780608657356357652"
timestamp: "2025-09-05"

Developer

Name: Ifan Alva

GitHub: @IfanAlva2

Discord: alzion_7

Experience: Backend developer with experience in smart contracts, API systems, and zero-knowledge integration for privacy-preserving applications.


Project

Name & Category

Project: zkThrottle — ZK-Based API Rate-Limiting

Category: infrastructure


Description

zkThrottle solves the problem of API abuse and privacy trade-offs in current rate-limiting solutions.
It provides a system where users can prove, using zero-knowledge proofs, that they have not exceeded their API usage quota (e.g., 100 calls/day) without exposing detailed usage logs.

API providers can enforce trustless, privacy-preserving rate-limits via the Soundness Layer + Sui, reducing abuse and centralization risks.

SL Integration

Use Soundness Layer to verify ZK proofs that counter ≤ limit.

Store verification results on Sui smart contracts for API backends to query.

Optionally integrate Walrus for storing usage commitments (counter states) for auditability.


Technical

Architecture

1. Client → generate ZK proof (counter ≤ limit)


2. Soundness Layer → verify proof


3. Sui Contract → log valid API calls


4. Backend API → serves only if valid flag exists


5. Walrus → optional commitment storage



Stack

Frontend: React (demo UI for developers)

Backend: Node.js (API gateway), Rust (prover service)

Blockchain: Soundness Layer + Sui

Storage: Walrus (commitments), local DB (counters)


Features

1. ZK proof of API quota compliance.


2. Trustless verification via Soundness Layer.


3. Sui contract registry for API call validation.


4. Optional Walrus audit trail for counter commitments.



Timeline

PoC (2-4 weeks)

[ ] Build simple circuit (counter ≤ N)

[ ] Integrate with SL verifier

[ ] Deploy basic ThrottleRegistry Move contract

[ ] Demo API backend + simple UI


MVP (4-8 weeks)

[ ] Add Walrus commitments

[ ] Release JS SDK (zkthrottle-client)

[ ] Expanded Move contract with quota/NFT management

[ ] Public test with ≥20 users


Innovation

First ZK-powered rate-limiting system for APIs.
Moves away from centralized API key systems and log-based monitoring.
Practical use-case for developers of AI, DeFi, or any high-demand service needing fair-use access.
Balances privacy + trustless enforcement.

Contact

Preferred: Discord (alzion_7)
