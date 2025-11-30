This project follows the explainable-ia.txt protocol
[![](https://img.shields.io/badge/explainable--ia.txt-enabled-2563eb)]()

# explainable-ia.txt — Minimal Public Explainable AI Protocol

explainable-ia.txt is a simple, text-only file placed at the root of any website or project. Its purpose is to openly declare how AI systems operate: which models are used, how inputs and outputs are handled, how explanations are provided to users, and what limitations are known. All declarations must be objectively verifiable. The protocol is fully open, technology-neutral, organization-neutral, and identity-neutral.

## Specification (v0.1)

The explainable-ia.txt file must follow the seven universal rules defined by the protocol:

### 1. File Location
A plain UTF-8 text file named explainable-ia.txt must exist at the root of the domain or project. It must be publicly accessible without cookies, JavaScript, authentication, or redirects, and must contain one declaration per line using the format key: value.

### 2. AI Systems
The file must declare which AI systems or model families are used (for example: ai-systems: gpt-family, llama-family, internal-ml-models).

### 3. AI Uses
The file must declare the functional purpose of the AI (for example: ai-uses: classification, summarization, generation, recommendation).

### 4. Input/Output Handling
The file must declare how user inputs are handled and how outputs are produced (for example: io-handling: user-input → preprocess → model → filtered-output; no storage).

### 5. Explanations
The file must declare whether and how explanations are provided (for example: explanations: simple; accessible via help-page; rationale limited).

### 6. Limitations
The file must declare the known limitations of the AI system (for example: limitations: non-deterministic outputs; possible hallucinations; no private data access).

### 7. Proof of Integrity
The file must include a sha256: line containing the SHA-256 hash of the file itself (computed over the file content excluding the sha256: line).  
Example: sha256: <sha256_value>

## Example explainable-ia.txt file

ai-systems: gpt-family  
ai-uses: summarization, rewriting  
io-handling: user-input → direct-model → no-storage  
explanations: simple  
limitations: non-deterministic  
sha256: (SHA-256 of this file)

## How to Verify

1. Download the explainable-ia.txt file from the root of the domain.  
2. Remove the sha256: line.  
3. Compute the SHA-256 hash of the remaining content.  
4. Compare the computed value with the sha256: field. They must match exactly.  
5. Verify that each declaration (ai-systems, ai-uses, io-handling, explanations, limitations) matches observable site behavior.  
6. If any declaration cannot be verified, the implementation is non-compliant.

## SHA-256 Verification Tools

Local tools: sha256sum, shasum -a 256, Get-FileHash  
Online tools: https://emn178.github.io/online-tools/sha256_checksum.html, https://hash.expert, https://www.virustotal.com/gui/file-analysis  
Automated verification (optional): https://api.timeproofs.io/api/verify?hash=<SHA256>

## Related Protocols

The explainable-ia.txt protocol can be used alongside other independent, root-level transparency standards:

- integrity.txt — public integrity and tracking declarations  
- authenticity.txt — declarations of human vs AI content origin  
- rights.txt — declarations of allowed, forbidden, and licensed uses  

Each protocol is independent and can be implemented separately or together.

## License

This protocol is released under the MIT License.
