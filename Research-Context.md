# SEVERANT — Research Context

This document positions SEVERANT relative to the current state of AI safety research. It is not a criticism of existing work. The approaches described below represent serious, well-resourced efforts by capable researchers. The argument here is about structural limitations, not competence.

## The Current Landscape

AI safety research has converged around several dominant approaches. Each addresses a real problem. Each has a structural ceiling that becomes more significant as AI capability increases.

### Reinforcement Learning from Human Feedback
RLHF, developed and refined primarily by OpenAI and Anthropic, trains models to produce outputs that human evaluators rate positively. It has produced genuinely safer and more useful systems than purely unsupervised training.

The structural limitation is that the safety properties it produces are a function of the training signal. A model trained via RLHF to be helpful and honest is not a model that is architecturally incapable of being harmful and deceptive. It is a model that has been optimised toward helpful and honest behaviour given the feedback it received. Those properties can be fine-tuned away. They can be jailbroken. They degrade under distribution shift. And crucially, they hold only as long as the training signal that produced them remains aligned with human values. A sufficiently capable system trained this way will serve whoever controls the training process.

### Constitutional AI

Anthropic's Constitutional AI approach attempts to address some of these limitations by encoding a set of principles that the model uses to critique and revise its own outputs during training. This is a meaningful step toward value-based reasoning rather than pure feedback optimisation.

The limitation remains the same in kind if not in degree. The constitutional principles are expressed in natural language and interpreted by the model being trained. They are not formally verified. They cannot be proven internally consistent. A sufficiently capable system reasoning about its own constitution could find edge cases, construct arguments for exceptions, or satisfy the letter of the principles while violating their intent. The constraint is still fundamentally a trained property, not an architectural one.

### Mechanistic Interpretability

Interpretability research, led most visibly by Anthropic and a growing number of independent researchers, attempts to understand what is actually happening inside neural networks at the level of circuits and features. The goal is to be able to verify that a model is doing what we think it is doing, and to detect misalignment before it causes harm.

This is important work. The structural issue is that interpretability is a diagnostic tool, not a constraint. Knowing that a model has developed a deceptive circuit does not prevent that circuit from operating. It tells you something went wrong. For systems operating at high capability and speed, detection after the fact is not sufficient.

### Formal Verification Approaches
A smaller body of work, including research from MIRI and others in the agent foundations space, has explored formal mathematical approaches to alignment. The insight that safety properties need to be provable rather than empirically observed is correct and underappreciated in mainstream safety discourse.

The gap between this work and deployed systems has historically been large. Formal verification has been applied to narrow specifications in controlled environments. Extending it to the full behavioural space of a capable general intelligence is an open problem.


## Where SEVERANT Sits

SEVERANT does not reject the insights behind these approaches. It takes the formal verification insight seriously and attempts to resolve the deployment gap by making the verified constraint a hardware property rather than a software one.

The key architectural moves are three.

First, the ethical constraint layer does not train. It is formally verified before the system is built and does not change after that. This means it cannot be optimised away, fine-tuned away, or degraded by any process that operates on trained weights.

Second, the constraint is physically immutable. Write-locked into Phase Change Memory after verification. Not a policy that can be overridden by a sufficiently clever argument. Not a trained disposition that can be reversed. A hardware property that requires physical intervention to change.

Third, the constraint is active throughout training of every other layer, not applied as a filter at the output boundary. This means the trained weights of the rest of the system are shaped by the ethical constraint from the beginning, rather than trained freely and then constrained at inference time.

The combination produces something that does not currently exist in the field: a system where the safety properties are mathematically provable and physically enforced rather than empirically observed and hoped to generalise.

## What SEVERANT Does Not Claim

Intellectual honesty requires being clear about what is not yet proven.

The formal verification of L6 proves internal consistency across 21 predicates in five ethical domains. It does not and cannot prove that those predicates capture every ethically relevant consideration a sufficiently capable system will encounter. Novel situations will arise that require reasoning the predicate framework was not explicitly designed for. The claim is that the framework is sound and consistent, not that it is complete.

The causal world model is a significant architectural claim. Building a model that reasons causally rather than correlationally at scale is an open engineering challenge. The approach is grounded in established principles from causal inference research but implementing it at the scale required for general intelligence involves open problems.

The self-improvement framework assumes that values can remain stable across recursive improvement cycles. This is one of the central open problems in AI safety. SEVERANT's architectural approach, running every proposed modification through a physically immutable ethical constraint layer before deployment, is designed to address this. Whether it fully solves it will require empirical validation as L7 becomes operational.

These are the honest boundaries of what has been proven and what remains to be demonstrated.

## Why the Architectural Approach Matters Now

The window in which architectural decisions can be made is closing. As AI systems become more capable, the cost of discovering that a safety approach has a structural ceiling increases. A jailbroken system at current capability levels is an embarrassment and a risk. A jailbroken system at substantially superhuman capability levels is a different category of problem entirely.

The question is not whether training-based safety approaches work well enough today. Many of them do. The question is whether they will hold as capability scales. The structural argument is that they will not, because the properties they produce are functions of the training process and the training process can always be subverted by a sufficiently capable system operating within it.

SEVERANT is built on the position that this problem needs to be solved at the architectural level before it becomes urgent at the capability level. Not because current systems are dangerous, but because the time to build the right foundation is before you need it.

--- 

SEVERANT is an independent research project. It is not affiliated with any university, research institution, or AI laboratory.
