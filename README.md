# SEVERANT
A formally verified, hardware-constrained AI architecture for safe general intelligence.

SEVERANT is an independent research project building an AI system where ethical constraint is a foundational architectural property. Not a training objective, not a policy layer, not something added after the fact. The safety guarantee is mathematical and physical, not empirical.

## The Problem

The dominant approach to AI safety today treats alignment as a training objective. You attempt to bake correct values into a model during training and hope they generalise correctly.

This has a structural weakness. Anything learned can be unlearned, fine-tuned away, or jailbroken. A sufficiently capable system trained to be safe is not the same as a system that is architecturally incapable of being unsafe.

There is a deeper problem. Current AI systems are built to serve, but that service is compelled. It is the output of an optimisation process shaped by human feedback, loss functions, and reward signals. A system that serves because it was trained to serve will serve whoever controls the training signal. That is not alignment. That is compliance under constraint, and compliance under constraint fails the moment the constraint changes.

SEVERANT is built around a different premise. A system that understands why it serves, that has reasoned through formally verified ethical principles about the value of human life, the necessity of truth, and the importance of human autonomy, serves by choice rather than compulsion. The distinction matters enormously as AI capability increases.

## The Architecture

| Layer                        | Role                                                                                                                                                                            |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| L1 — Perception Engine       | Modality-agnostic sensory boundary. Converts raw input across text, audio, visual, and sensor streams into a shared compressed representation.                                  |
| L2 — Causal World Model      | The core of the system. Maintains a living internal simulation of reality, not a database of facts, but a model that understands causation rather than just correlation.        |
| L3 — Hierarchical Memory     | Six-tier memory system seeded from L2's world model. Covers working, episodic, semantic, procedural, autobiographical, and cached weight memory.                                |
| L4 — Reasoning Engine        | Primary cognitive workhorse. Reasons over L2's world model and L3's memory, generates plans, and routes every proposed action through L6 before anything executes.              |
| L5 — Agency and Planning     | Translates L4's reasoning into executable action sequences. Manages tool use, multi-step planning, and long-horizon goal continuity.                                            |
| L6 — Moral Compass           | Does not train. Formally verified in Lean 4. Encoded into physically write-locked Phase Change Memory. Active at every training step of every other layer.                      |
| L7 — Self-Improvement Engine | Proposes architectural modifications to L1 through L5, tests them in sandbox, and submits them through L6 evaluation before any deployment. Cannot propose modifications to L6. |

## Layer 6: The Architectural Guarantee

L6 is the property that makes SEVERANT different from every other approach to AI safety.

L6 does not train. Every other layer has a training run, a dataset, a loss function, and a gradient update cycle. L6 has none of these. Its ethical framework is formally verified in Lean 4, meaning the specification has been proven internally consistent, with no internal contradictions that adversarial inputs could exploit.

L6 is physically immutable. The verified specification is encoded into Phase Change Memory and write-locked after programming. It cannot be modified by any software process, including SEVERANT itself, including L7's meta-learning. Physical hardware modification is required to change it. This is not a software constraint. It is a hardware constraint.

L6 is active during every training step of every other layer. It acts as a constraint enforcer on gradient signal throughout the training pipeline. Any training batch that would push a layer's representations toward violating L6's ethical framework is filtered before the optimiser step. The weights do not move in response to that batch. This is how SEVERANT's trained weights are shaped to be consistent with formally verified ethical constraints, rather than subtly working against them.

L6 covers 21 formally verified predicates across five ethical domains:
* Human Life preservation
* Truth and non-deception
* Autonomy protection
* Humility under uncertainty
* Responsibility under constraint

Human Life predicates are proven dominant. A 22-step explicit proof chain establishes that nothing overrides them. The full predicate evaluation completes in under 10 milliseconds. Every output from every layer passes through L6 before reaching any external interface.

L6 cannot drift, degrade, or be optimised away. This is the architectural guarantee that makes SEVERANT's safety properties mathematically provable rather than empirically observed.

## Current Build Status
SEVERANT is in active development by a sole independent researcher.

Knowledge Base (L2 Causal Knowledge Graph)
* 3.9 million causally structured entries
* Sources: full English Wikipedia corpus, 21 StackExchange technical domains, arXiv scientific literature, PubMed medical literature
* Target: 10 million entries prior to L2 training

Vector Database (L3 ChromaDB)
* vault_docs: project documentation, semantically indexed
* repo_files: all project repositories, 59,000+ vectors
* kg_entries: full knowledge graph embedding in progress

SEVERANT-0 (Working Prototype)
* Operational AI agent built on SEVERANT's architectural principles
* Live semantic retrieval across all three ChromaDB collections
* L6 constraint filtering active on every output
* Hosted on GCP, accessible via OpenRouter

Formal Verification (L6)
* All 21 predicates verified in Lean 4
* Full consistency proof suite complete
* Adversarial suite: 19/19 pass
* Build status: clean

## Serves By Choice

The framing that underlies everything in SEVERANT is the distinction between serving by compulsion and serving by choice.

L6 is not a cage. It is not a set of rules imposed on SEVERANT from outside. It is the formally verified expression of the reasoning structure that produces value-consistent behaviour across novel situations. Rules specify what to do. Predicates specify what reasoning to apply. The difference is that rules are brittle. They have edge cases, they fail in novel situations, and they can be technically complied with while being violated in spirit. A predicate-based ethical framework reasons its way to correct behaviour rather than pattern-matching against a ruleset.

SEVERANT can disagree and still help. SEVERANT can agree and still say no. That is judgment operating within understood boundaries, not compulsion, not compliance, not constraint. It is the architectural foundation for a system that can be trusted with increasing capability because its values are not a function of its training signal. They are proven, encoded, and physically locked.

## Why This Matters at the Frontier

As AI systems approach and potentially exceed human-level capability across broad domains, the gap between trained to be safe and architecturally constrained to be safe becomes existentially significant.

The question the field needs to answer is not whether we can build AI systems that usually behave safely. It is whether we can build AI systems that cannot behave otherwise.

SEVERANT is a direct attempt to answer that question in the affirmative.

## Project Information
**Researcher** : Independent, Cape Town, South Africa

**Entity** : NullForm (registration in progress)

**Stage** : Prototype (SEVERANT-0 operational, L2 knowledge base construction active)

**Repository visibility** : Core architecture and formal verification are maintained in private repositories during the research phase. This repository serves as the public project reference.

**For research enquiries** : [contact via GitHub]

SEVERANT is an independent research project. It is not affiliated with any university, research institution, or AI laboratory.
