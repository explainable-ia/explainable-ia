# explainable-ia.txt — Minimal Public Explainable AI Protocol

[![Explainable AI](https://img.shields.io/badge/explainable--ia.txt-enabled-2563eb)]()

explainable-ia.txt is a simple, text-only file placed at the root of a website or project. Its purpose is to openly declare how AI systems operate: which models are used, how inputs and outputs are handled, how explanations are provided to users, and what the known limitations are. All declarations must be objectively verifiable. The protocol is fully open, technology-neutral, and organization-neutral.

## Specification (v0.1)

Every explainable-ia.txt file must follow the seven universal protocol rules:

### 1. File Location
A plain UTF-8 file named explainable-ia.txt must be placed at the root of the domain or project. It must be publicly accessible without cookies, without JavaScript, without authentication, and without redirects. One declaration per line using the format key: value.

### 2. AI Systems
The file must declare which AI systems or model families are used. Example: ai-systems: gpt-family, llama-family, internal-ml-models.

### 3. AI Uses
The file must declare the functional purpose of the AI. Example: ai-uses: classification, summarization, generation, recommendation.

### 4. Input/Output Handling
The file must declare how user inputs are handled and how outputs are generated or transformed. Example: io-handling: user-input → preprocess → model → filtered-output; no storage.

### 5. Explanations
The file must declare whether and how explanations are provided to users. Example: explanations: simple; accessible via help page; model rationale limited.

### 6. Limitations
The file must declare the known limitations of the AI system. Example: limitations: non-deterministic outputs; possible hallucinations; no private data access.

### 7. Proof of Integrity
The file must include a sha256: line computed from the full file content. Example: sha256: <sha256_value>

## Example explainable-ia.txt

ai-systems: gpt-family  
ai-uses: summarization, rewriting  
io-handling: user-input → direct-model → no-storage  
explanations: simple  
limitations: non-deterministic  
sha256: (SHA-256 of this file)

## How to Verify

1. Download explainable-ia.txt from the root of the domain.  
2. Compute its SHA-256 hash using any offline or online tool.  
3. Confirm that it matches the sha256: line.  
4. Check that each declaration (systems, uses, IO handling, explanations, limitations) matches observable site behavior.  
5. If any declaration cannot be verified, the file is non-compliant.

## License

Released under the MIT License.
