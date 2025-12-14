# Explicit Semantic Commitment Layer

A minimal open-source layer enabling users to explicitly declare the meaning they assign to terms,  
and requiring AI systems to treat these declarations as persistent semantic commitments.

This repository implements a missing infrastructural capability for human-centered AI systems:  
the recognition of **explicit user-defined meaning as a normative constraint**, rather than as transient conversational context.

---

## 1. Problem

Contemporary AI systems, including large language models (LLMs), are highly effective at adapting to conversational context.  
They can temporarily follow a user’s vocabulary, framing, or perspective during an interaction.

However, they do not recognize the user as an authoritative source of meaning.

When a user states:

> “When I say X, I mean Y.”

this declaration is treated as contextual information, not as a binding semantic commitment.

As a result:
- meanings are not persistent across interactions,
- user-defined definitions can be overridden by statistical norms,
- semantic ambiguity reappears over time,
- meaningful comparison between individuals is impossible.

This limitation is architectural, not computational.

---

## 2. What Existing Systems Do

Current AI systems can:
- adapt locally to user language,
- maintain short-term conversational coherence,
- infer probable meanings statistically.

They cannot:
- store explicit user-defined meanings as durable entities,
- treat these meanings as normative constraints,
- assign semantic authority to the human user,
- compare meanings across individuals without collapsing them into averages.

The issue is not model performance, but the absence of a semantic commitment layer.

---

## 3. Contribution of This Repository

This repository provides a minimal implementation of a **semantic commitment layer** that enables:

- explicit declaration of meaning by the user,
- persistence of declared meanings over time,
- priority of declared meaning over inferred meaning,
- revision authority restricted to the declaring user,
- comparison of semantic commitments between users.

The layer is designed to operate **on top of existing AI systems**, without modifying their internal architecture.

---

## 4. Core Principles

1. Human Semantic Authority  
   The user is the sole authority over the meaning they assign to their own terms.

2. Explicitness  
   Meaning is declared, not inferred.

3. Persistence  
   Declared meanings remain active until explicitly revised by the user.

4. Priority  
   Semantic commitments take precedence over statistical or inferred interpretations.

5. Non-Resolution  
   Divergent meanings are made visible but are not automatically resolved.

---

## 5. Minimal Architecture

The system consists of four components:

- Semantic Commitment Registry  
  Stores declared meanings with metadata (author, timestamp, version, status).

- Normative Rules  
  Enforce priority, persistence, and revision constraints.

- Comparison Module  
  Identifies overlap, divergence, or absence between semantic commitments.

- API Interface  
  Allows external systems to query and respect declared commitments.

No semantic parsing, ontology, or inference engine is included.

---

## 6. Example: Single User

User declaration:

> “When I say ‘beauty’, I mean an abstract relational concept, not an aesthetic property.”

The system records this declaration as an active semantic commitment.

Any AI system interacting with this user is required to:
- retrieve the commitment,
- treat it as normative,
- avoid reverting to conventional definitions unless explicitly allowed by the user.

---

## 7. Example: Two Users

User A:
> “When I say ‘freedom’, I mean individual autonomy.”

User B:
> “When I say ‘freedom’, I mean collective self-determination.”

The system:
- records both commitments independently,
- detects semantic divergence,
- exposes the difference without enforcing resolution.

This enables meaningful dialogue without forced consensus.

---

## 8. Scope

This repository focuses exclusively on:
- explicit declaration of meaning,
- persistence and revision,
- semantic comparison.

It does not address:
- ethical governance frameworks,
- peer-to-peer or distributed architectures,
- blockchain or ledger technologies,
- economic models,
- validation of semantic truth.

These concerns belong to higher-level infrastructures.

---

## 9. Limitations

- The system does not interpret or understand meaning.
- No claim is made regarding semantic correctness or truth.
- The quality of commitments depends on human clarity and good faith.
- Ambiguity is not eliminated, but made explicit.

These limitations are intentional.

---

## 10. Integration

The semantic commitment layer can be integrated with:
- proprietary language models,
- open-source LLMs,
- chat-based interfaces,
- educational or collaborative platforms.

Integration requires only that the host system consult the registry before generating or interpreting language.

---

## 11. Citation

If you use this work in academic research, please cite it using the provided `CITATION.cff` file.

---

## 12. License

This project is released under the MIT License.  
See the `LICENSE` file for details.
