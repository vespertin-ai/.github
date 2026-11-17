# Vespertin

**The evidence layer for human-governed agent fleets.**

Routine steps run on written policy rules. Consequential steps wait for a named operator, and every decision seals into cryptographic proof that anyone can verify offline without our servers.

[vespertin.io](https://vespertin.io) · [Offline Receipt Verifier](https://vespertin.io/verify.html) · [Security Policy](https://github.com/vespertin-ai/.github/blob/main/SECURITY.md)

---

## Architecture

### 1. Reflex Gate (`GREEN` · `YELLOW` · `RED` · `NEVER`)
Every consequential verb receives a policy tier before execution. Routine actions run within explicit bounds (`GREEN` and `YELLOW`). Ungranted or high-impact actions hold in `RED` until a named person settles them. Self-approval and policy tampering land in `NEVER`.

### 2. Human Seat
Approvals bind to a named, authenticated operator through hardware-backed FIDO2 WebAuthn (`BE=0`) or enrolled Ed25519 keys. Notifications inform operators, but bearer tokens never co-sign a settlement.

### 3. Append-Only Chain (`Marrow`)
Each sealed decision records the BLAKE3 digest of the previous entry inside a signed DSSE envelope over RFC 8785 canonical JSON. Auditors and counterparties recompute the full Ed25519 signature and hash chain offline using public keys alone.

---

## Standalone Offline Verification

Download [verify.html](https://vespertin.io/verify.html), disconnect from the network, and verify signed decision bundles in any browser through embedded zero-import WebAssembly (`marrow-verify-wasm`).
