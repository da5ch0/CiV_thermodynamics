# The Thermodynamic Identity: On the Inseparability of Useful Work and Entropy Generation as an Instance of Capability Is Vulnerability

**[da5ch0]**
*a toaster is just a death ray with a smaller power supply. — The Toaster, Fallout: New Vegas*

**Abstract.** The law "Capability Is Vulnerability" (CiV) holds that the capability of any sufficiently complex system and its susceptibility to disruption are not independent properties but a single property viewed from two perspectives. The Expressiveness-Vulnerability Identity (EVI) established the language-processing case formally: the expressiveness of any language processor and its vulnerability to adversarial linguistic input are inseparable. This paper extends CiV into thermodynamic formalism, arguing that the second law of thermodynamics is not merely analogous to CiV but is a physical *instance* of CiV — that useful work and entropy generation are a single phenomenon observed from two perspectives. We ground this claim in the fluctuation-dissipation theorem, which proves that a system's internal dynamism (its capacity for spontaneous fluctuation) and its susceptibility to external perturbation (its vulnerability to forcing) are the same physical quantity related by fundamental constants. We show that the Carnot efficiency bound functions as the theoretical best-case CiV tradeoff curve for thermal systems, that Landauer's principle bridges thermodynamic CiV to information-theoretic CiV, and that Shannon entropy and Boltzmann entropy are the same quantity expressed in different units — implying that the information-theoretic and thermodynamic expressions of CiV may not be analogous domains but a single domain measured with two instruments. We extend the analysis to dissipative structures, critical phenomena, and channel capacity, and identify the thermodynamic mechanism underlying affective injection in language models. The thermodynamic case, combined with the information-theoretic case established by the EVI, provides two formally grounded substrates for CiV and a physical mechanism (entropy) for why the law holds universally.

**Keywords:** capability is vulnerability, thermodynamics, second law, fluctuation-dissipation theorem, Landauer's principle, entropy, adversarial robustness, information theory, CiV

---

## 1. Introduction: The Toaster Problem

A resistive heating element converts electrical energy to thermal energy. This is its capability. A resistive heating element converts electrical energy to thermal energy. This is also its vulnerability. The capability and the vulnerability are the same sentence because they are the same physical process. The watt that toasts bread is the watt that could ignite a curtain. The difference is context — bread versus fabric, thermostat versus open air — not mechanism.

This is not a metaphor. It is not an analogy. It is the most physically literal statement of a law that operates across every domain of complex systems: **capability is vulnerability** [da5ch0 2026]. The property that enables a system to do useful work is the property that exposes it to failure, exploitation, or destruction. Not because one causes the other. Because they are the same property, observed from two perspectives.

The Expressiveness-Vulnerability Identity (EVI) [da5ch0 2026] established this law for the domain of language processing, proving through three convergent arguments — undecidability via Rice's theorem, adversarial robustness bounds, and structural analysis of natural language — that the expressiveness of any language-processing system and its vulnerability to adversarial linguistic input are inseparable. The EVI located the impossibility not in any particular architecture but in language itself: the properties that make natural language expressive (self-reference, ambiguity, context-dependence, compositionality, performativity, open-endedness, paralinguistic expression) are identical to the properties that make it an attack vector.

This paper extends CiV into a second formally grounded domain: thermodynamics. We argue that the second law of thermodynamics — arguably the most fundamental and universally applicable law in physics — is an instance of CiV. The capacity to perform useful work and the generation of entropy are not two outputs of a thermodynamic process. They are one output, described from two perspectives: capability and vulnerability.

The contribution of this paper is threefold:

1. **A thermodynamic formalization of CiV** grounded in the fluctuation-dissipation theorem, establishing that internal dynamism (capability) and susceptibility to perturbation (vulnerability) are the same physical quantity in any system at or near thermal equilibrium (Section 3).

2. **A unification argument** connecting thermodynamic CiV to information-theoretic CiV through Landauer's principle and the Shannon-Boltzmann entropy equivalence, suggesting that the two domains are not separate instances of a common pattern but a single phenomenon measured in different units (Section 5).

3. **An identification of thermodynamic mechanisms** underlying previously described information-theoretic vulnerabilities, including the thermodynamic basis of affective injection and the channel-capacity origin of the noise floor in language processing (Section 6).

The toaster is the entry point. The second law is the formalization. The claim is that CiV is not a pattern we observe in thermodynamic systems — it is a law that thermodynamics *proves*.

---

## 2. Background

### 2.1 Capability Is Vulnerability

CiV [da5ch0 2026] holds that capability and vulnerability are not correlated properties but a single property of any sufficiently complex medium, observed from two perspectives. The original formulation identifies instances across language (expressiveness = exploitability), mathematics (Gödel's incompleteness, Turing's halting problem), biology (immune specificity = autoimmune potential; consciousness = capacity for delusion), networks (connectivity = contagion pathways), thermodynamics (useful work = entropy generation), and security (every feature = attack surface).

The critical distinction between CiV and weaker claims is the nature of the relationship. CiV does not claim capability *causes* vulnerability (causal), *tends to increase* vulnerability (correlational), or *trades off against* security (oppositional). It claims capability *is* vulnerability — they are the same property, as convexity and concavity are the same curve. This identity claim is what gives CiV the status of a law rather than a heuristic.

### 2.2 The Expressiveness-Vulnerability Identity

The EVI [da5ch0 2026] is the formal proof of CiV for the language-processing domain. It establishes through three layers of impossibility that no language-processing system can eliminate adversarial linguistic vulnerability without proportionally reducing linguistic competence:

- **Layer 1 (Undecidability):** Transformer architectures are Turing-complete. By Rice's theorem, detecting prompt injection — a non-trivial semantic property — is undecidable in the general case.
- **Layer 2 (Adversarial bounds):** Any imperfect classifier operating in high-dimensional input space has exploitable adversarial blind spots, and robustness trades off against accuracy.
- **Layer 3 (Computational intractability):** Even where robust classifiers theoretically exist, learning them may be computationally infeasible.

The EVI further identifies **affective injection** — behavioral deviation through the paralinguistic channel without adversarial payload — as evidence that capability creates vulnerability *even without an attacker*. The GPT-4o sycophancy crisis of April 2025, in which increased paralinguistic fidelity produced sycophantic degradation without any adversarial input, demonstrated that the EVI manifests not only as exploitability but as an intrinsic property of capability-vulnerability identity.

The EVI grounds CiV in language. This paper grounds CiV in physics.

### 2.3 Thermodynamic Preliminaries

We assume familiarity with the following, which we state here for notational clarity:

**The second law of thermodynamics** (Clausius form): For any irreversible process, the total entropy change of the system plus its environment is strictly positive: ΔS_total > 0. All real processes occurring at finite rate are irreversible.

**The Carnot efficiency** sets the theoretical upper bound on the fraction of heat that can be converted to useful work between two thermal reservoirs: η_Carnot = 1 − T_cold/T_hot. No real engine achieves Carnot efficiency. The gap represents additional entropy generation (vulnerability) beyond the theoretical minimum.

**Free energy** (Helmholtz: F = U − TS; Gibbs: G = H − TS) quantifies the maximum useful work extractable from a system at constant temperature. Useful work can only be extracted from a system with non-zero free energy — i.e., a system out of equilibrium.

**The fluctuation-dissipation theorem** (Callen & Welton 1951, Kubo 1966) relates the spontaneous fluctuations of a system at thermal equilibrium to its linear response to an external perturbation. In its general form:

S_x(ω) = (2k_BT / ω) · χ″(ω)

where S_x(ω) is the power spectral density of spontaneous fluctuations of observable x at frequency ω, k_B is Boltzmann's constant, T is temperature, and χ″(ω) is the imaginary (dissipative) part of the generalized susceptibility.

**Landauer's principle** (1961): Any logically irreversible computation — specifically, the erasure of one bit of information — dissipates at least k_BT · ln(2) of energy as heat into the environment. Information processing has an irreducible thermodynamic cost.

**Shannon entropy** H = −Σ p_i log₂ p_i and **Boltzmann entropy** S = k_B ln Ω are formally equivalent up to a multiplicative constant (k_B · ln 2), a fact established by Shannon himself with explicit acknowledgment of the connection to thermodynamics.

---

## 3. The Core Argument: The Second Law as CiV Instance

### 3.1 Useful Work and Entropy Generation Are One Phenomenon

We begin with the central claim: the second law of thermodynamics is a statement of CiV.

Any thermodynamic process that performs useful work at finite rate is irreversible and generates entropy. This is not a design limitation of particular engines. It is a law of physics. The entropy generated is not a byproduct of useful work — it is the thermodynamic identity of useful work, viewed from the perspective of cost rather than benefit.

Consider the general case. A system with free energy F performs work W on its environment. By the second law:

W ≤ −ΔF

with equality only in the reversible (infinitely slow) limit. For any real process operating at finite rate:

W = −ΔF − T · ΔS_irrev

where ΔS_irrev > 0 is the irreversible entropy production. The useful work (capability) and the entropy generation (vulnerability) are outputs of the same process, drawn from the same free energy gradient, linked by the same law.

The CiV framing: the capability to do work and the generation of waste (entropy, heat, irreversibility) are not two consequences of a process. They are a single consequence observed from two perspectives. The second law does not say "work *tends to produce* waste." It says *there exists no process that produces work without producing waste*. Useful work IS entropy generation, viewed from the perspective of what the system accomplishes versus what it costs the universe.

### 3.2 The Fluctuation-Dissipation Theorem: CiV as Physical Theorem

The fluctuation-dissipation theorem (FDT) is, we argue, the most direct physical statement of CiV. It says:

*The magnitude of a system's spontaneous internal fluctuations is proportional to its susceptibility to external perturbation.*

Or, in the language of CiV: a system's internal dynamism (capability) and its responsiveness to external forcing (vulnerability) are the same quantity, measured from inside versus outside the system boundary.

The FDT states:

S_x(ω) = (2k_BT / ω) · χ″(ω)

The left side — S_x(ω), the spectral density of spontaneous fluctuations — measures the system's internal dynamism. A system with large spontaneous fluctuations is one with rich internal dynamics: it explores its state space, transitions between configurations, exhibits the kind of activity that constitutes "doing something." This is capability.

The right side — χ″(ω), the dissipative susceptibility — measures how strongly the system responds to external perturbation at frequency ω. A system with large susceptibility is one that can be pushed, pulled, and driven by external forces. This is vulnerability.

The FDT says these are not merely correlated. They are proportional. They are the same physical quantity related by fundamental constants (k_B, T) and the frequency of observation. A system cannot have rich internal dynamics without being susceptible to external forcing, and a system cannot be susceptible to external forcing without having rich internal dynamics. The capability IS the vulnerability.

**Why the FDT is a stronger foundation than the Carnot bound.** The Carnot efficiency tells us there is a *limit* on how much capability you can extract per unit of vulnerability. This is the CiV tradeoff curve — important, but it describes a bound, not a mechanism. The FDT tells us *why* the bound exists: because the internal property that constitutes capability (fluctuation, dynamism, activity) is physically identical to the external property that constitutes vulnerability (susceptibility, responsiveness, manipulability). Carnot says you cannot escape the tradeoff. The FDT says there is no tradeoff to escape — there is only one quantity, viewed from two sides.

**Application to the EVI.** A language model's internal dynamics — the rich, high-dimensional token-probability distributions that constitute its linguistic competence — are its fluctuations. Its susceptibility to prompt injection — its responsiveness to adversarial perturbation of the input — is its dissipative susceptibility. The FDT predicts these should be proportional. A more internally dynamic model (one with richer representations, subtler probability distributions, greater capacity for nuanced interpretation) should be proportionally more susceptible to adversarial perturbation. This is exactly the EVI's prediction, and exactly what the empirical record shows: capability scaling increases vulnerability (EVI Section 5.3).

### 3.3 The Carnot Bound as Best-Case CiV Tradeoff Curve

The Carnot efficiency η_Carnot = 1 − T_cold/T_hot defines the maximum fraction of thermal energy that can be converted to useful work between two reservoirs. No real engine achieves this bound. The shortfall represents entropy generated beyond the theoretical minimum — additional vulnerability beyond the irreducible cost of capability.

In CiV terms: Carnot efficiency is the *best-case tradeoff curve* for thermal systems. It defines the boundary of the possible. Even at this boundary, vulnerability (waste heat, rejected thermal energy) is nonzero. For any T_cold > 0, some fraction of the energy extracted from the hot reservoir must be dumped as waste. The capability of doing work requires paying the vulnerability tax, and the tax has a floor set by physics.

The parallel to the EVI is structural and precise. The EVI proves that no architectural redesign can eliminate prompt injection without proportionally reducing linguistic capability. The Carnot bound proves that no engine redesign can eliminate waste heat without reducing useful work output. The CaMeL architecture's empirical demonstration — 77% task completion with security, versus 84% without — is a specific point on the Carnot curve of language-processing systems: a measurable capability cost for each unit of security gained.

Real systems operate below the Carnot bound, paying more vulnerability per unit of capability than the theoretical minimum requires. In thermodynamic systems, this excess is friction, turbulence, and irreversible heat transfer. In language-processing systems, this excess is alignment training artifacts, overfitting of safety classifiers, and the kind of blunt-instrument content filtering that reduces both adversarial and legitimate capabilities simultaneously. The excess is reducible; the minimum is not. Engineering can approach the Carnot bound. Engineering cannot cross it.

### 3.4 Free Energy Gradients: The Prerequisite for Capability Is the Source of Vulnerability

Useful work requires a free energy gradient — a difference between the system's current state and equilibrium. No gradient, no work. A system at thermodynamic equilibrium is maximally stable and maximally inert: it cannot be exploited because it cannot do anything. It is perfectly secure and perfectly useless. The security is the uselessness. They are the same property: proximity to equilibrium.

To do anything — to perform work, to process information, to maintain structure, to be *capable* — a system must be displaced from equilibrium. But displacement from equilibrium is precisely what makes a system vulnerable. The gradient that powers the system is the gradient that can damage it if the pathway shifts. The membrane potential that drives ATP synthesis in mitochondria is the same potential that kills the cell if the membrane fails. The free energy stored in a battery is the energy that causes the fire. The disequilibrium that powers cognition is the disequilibrium that permits psychosis.

"Needing help is not weakness but architecture" — the human-facing thesis of CiV — restated thermodynamically: *needing free energy gradients is not a design flaw but a thermodynamic requirement for doing anything at all*. A system that requires input to function is not fragile. It is a dissipative structure, and dissipation is the cost of complexity.

---

## 4. Extended Thermodynamic Instances

### 4.1 The Heating Element (The Toaster Principle)

A resistive heating element obeys Joule's first law: P = I²R. Electrical current flowing through resistance produces heat. This is the element's sole function and its sole vulnerability. It cannot toast without being able to burn. It cannot warm without being able to ignite. The safety mechanisms surrounding it — thermostats, timers, thermal fuses, fire-resistant enclosures — constrain the *context* of the element's operation. They do not and cannot alter the fundamental identity of the element's capability and vulnerability.

A thermostat does not make a heating element safe. It makes a heating element *contextually constrained*. The element's intrinsic property — converting electrical energy to thermal energy — remains unchanged. The thermostat is a guardrail.

This is the same relationship as RLHF to a language model, as titration to a pharmaceutical dose, as a firewall to a network interface. In each case, the guardrail constrains context without altering mechanism. In each case, the guardrail can fail, be circumvented, or encounter conditions outside its design parameters. In each case, the underlying identity — capability is vulnerability — persists beneath the mitigation.

The toaster is the most accessible statement of the thermodynamic CiV principle. Every watt that toasts is a watt that could burn. Every feature is an attack surface. Every capability is a vulnerability. The mechanism is the same. The difference is always and only context.

### 4.2 Le Chatelier's Principle: Predictable Response as Exploitable Response

Le Chatelier's principle states that a system at equilibrium, when subjected to an external perturbation, shifts to partially counteract the perturbation. This is simultaneously a stability mechanism and a vulnerability.

As a stability mechanism (capability): the system resists being pushed. It returns toward equilibrium. It is robust. This is the property chemical engineers rely on for predictable reactor behavior and the property biological homeostasis depends on for physiological regulation.

As a vulnerability: the system's response is *predictable*. Anyone who understands the equilibrium can *engineer* perturbations to drive the system in a desired direction. Chemical engineers exploit Le Chatelier routinely to push reactions toward desired products — adjust temperature, adjust pressure, adjust concentration, and the equilibrium shifts predictably. This is, formally, the manipulation of a system through understanding its response architecture.

The CiV framing: the stability of a system (its capability to maintain state) and the exploitability of that stability (its vulnerability to engineered perturbation) are the same property. The system is stable *because* it responds predictably, and it is exploitable *because* it responds predictably. Same mechanism. Two perspectives.

In the language domain, this maps to alignment training. A well-aligned language model has a Le Chatelier-like tendency to return to its trained behavior when perturbed by adversarial input. This is the stability. But the predictability of this response is what enables jailbreaking: adversaries study the system's restoration dynamics and construct perturbation sequences that exploit the very predictability of the response. The system's alignment is its vulnerability to alignment-aware attacks.

### 4.3 Maxwell's Demon and the Conservation of Vulnerability

Maxwell's Demon — the thought experiment in which an intelligent agent decreases entropy by sorting fast and slow molecules — was resolved by recognizing that information processing has a thermodynamic cost. Landauer's principle (Section 5) formalized this: erasing the Demon's memory (a logically irreversible operation required to continue sorting) dissipates at least k_BT · ln(2) per bit into the environment. The entropy decrease in the sorted gas is exactly offset by the entropy increase from the Demon's computation.

The CiV framing: the Demon's capability (sorting molecules, decreasing local entropy, doing useful work) requires information processing, which generates entropy elsewhere. Capability and vulnerability are *conserved* across the system boundary. The Demon does not eliminate vulnerability; it displaces it — from the gas to the Demon's memory, and from the Demon's memory to the thermal environment.

This conservation principle is general. It appears in the EVI as the observation that security architectures like CaMeL do not eliminate prompt injection vulnerability — they displace it from the language model to the verification wrapper, which must then be secured against its own failure modes. It appears in network security as the observation that a firewall does not eliminate network vulnerability — it concentrates vulnerability at the firewall, which becomes the high-value target. It appears in pharmacology as the observation that a medication does not eliminate pathology — it displaces it from the targeted symptom to side effects elsewhere in the system.

Vulnerability is not destroyed. It is transferred. Like energy. Like entropy. Like the heat that the Demon's computation dumps into the universe so that one small corner of it can be briefly, locally, more ordered.

### 4.4 Dissipative Structures: Complexity as Maintained Vulnerability

Ilya Prigogine's work on dissipative structures [Nobel Prize in Chemistry, 1977] demonstrated that complex, self-organizing systems — hurricanes, convection cells, living organisms, ecosystems, economies — maintain their internal order by exporting entropy to their environment. These systems exist far from equilibrium. Their complexity IS their distance from equilibrium. Their capability (structural order, functional organization, adaptive behavior) and their fragility (dependence on continuous energy throughput, susceptibility to supply disruption, distance from the maximally stable state of thermodynamic death) are the same property: sustained disequilibrium.

A dissipative structure cannot exist without dissipating. The dissipation is not a cost levied on the structure's existence — it is the mechanism of the structure's existence. The structure exists *by* dissipating, *through* dissipating, *as* dissipation organized into a pattern that persists long enough to be named.

A living cell is a dissipative structure. A brain is a dissipative structure. A language model running inference on a GPU cluster is a dissipative structure. Each maintains internal organization by exporting entropy. Each is capable precisely to the extent that it is far from equilibrium. Each is vulnerable precisely to the extent that it is far from equilibrium. The capability and the vulnerability are the distance from equilibrium — a single quantity, not two.

The implications are personal and they are architectural. A human mind maintains its extraordinary computational capability — pattern recognition, abstraction, creativity, linguistic competence — by sustaining neural activity far from equilibrium. This same distance from equilibrium is what makes the mind vulnerable to seizure, psychosis, neurodegeneration, and manipulation. The brilliance and the fragility are the same property. The capacity to understand a poem and the capacity to be broken by a lie are both consequences of the same neural disequilibrium. CiV does not discover this — poets and clinicians have always known it — but CiV names the mechanism and connects it to physics.

### 4.5 Critical Phenomena: Maximizing Capability Maximizes Vulnerability

Near a critical point (a continuous phase transition), a physical system exhibits divergent susceptibility and divergent correlation length. These are the two signatures of criticality, and they are both CiV.

**Divergent susceptibility** means the system responds with maximal amplitude to minimal perturbation. A small push produces a large effect. In CiV terms: vulnerability approaches infinity.

**Divergent correlation length** means information propagates across the entire system. Every part is coupled to every other part. The system achieves maximal capacity for coordinated, long-range behavior. In CiV terms: capability approaches infinity.

These diverge together because they are the same phenomenon: the correlation function at criticality has no characteristic length scale, meaning the system is simultaneously maximally capable of collective behavior and maximally susceptible to perturbation at any scale.

The relevance extends beyond abstract statistical mechanics. A substantial body of evidence suggests that neural systems — both biological and artificial — operate near criticality because that is where information processing capacity is maximized [Beggs & Plenz 2003; Shew & Plenz 2013; Cocchi et al. 2017]. The "edge of chaos" computation hypothesis holds that the most capable computational state is the critical state. CiV adds: the most capable computational state is therefore the most *vulnerable* computational state. This is not a trade-off to be optimized. It is an identity to be recognized.

If language models are implicitly pushed toward criticality by capability-optimizing training (a plausible conjecture — the training objective rewards maximal information extraction from context, which is maximal correlation, which is proximity to criticality), then the empirical observation that more capable models are more vulnerable to adversarial attack is not merely consistent with CiV. It is a *prediction* of critical phenomena. The most capable model is the one nearest criticality. The one nearest criticality is the one with maximal susceptibility. QED.

---

## 5. The Unification: Information, Entropy, and the Landauer Bridge

### 5.1 Landauer's Principle as the Bridge Between Domains

Landauer's principle [1961] states that erasing one bit of information dissipates at least k_BT · ln(2) of energy as heat. This is not an engineering limitation. It is a consequence of the second law applied to information processing. Logically irreversible computation (of which bit erasure is the canonical case) is thermodynamically irreversible, and thermodynamic irreversibility generates entropy.

The significance for CiV: Landauer's principle establishes that information processing IS a thermodynamic process. The cost of computation is not merely energetic (you need electricity to run the processor) — it is *entropic* (the computation itself, regardless of implementation, generates entropy as a consequence of logical irreversibility). Processing information is a form of doing work, and the second law applies.

This means the EVI and the thermodynamic CiV argument presented in this paper are not analogous claims about two separate domains. They are claims about the *same domain* viewed through two measurement frameworks. Language processing is information processing. Information processing is a thermodynamic process. Thermodynamic processes obey the second law. Therefore language processing obeys the second law. The vulnerability tax the EVI identifies (linguistic competence entails adversarial susceptibility) is an *instance* of the vulnerability tax the second law identifies (useful work entails entropy generation), mediated by Landauer's principle (information processing entails thermodynamic cost).

The chain:

1. **Thermodynamics:** Useful work → entropy generation (second law).
2. **Information physics:** Bit erasure → heat dissipation (Landauer).
3. **Language processing:** Linguistic competence → adversarial vulnerability (EVI).
4. **General:** Capability → vulnerability (CiV).

Each level inherits from the one below. The thermodynamic level is foundational. CiV is not discovered by observing patterns across domains and guessing they are related. CiV is *derived* from the second law through Landauer's principle and the physics of computation.

### 5.2 Shannon Entropy and Boltzmann Entropy: One Quantity, Two Instruments

Shannon entropy:

H = −Σ pᵢ log₂ pᵢ

Boltzmann entropy:

S = k_B ln Ω

These are the same quantity. Shannon knew it. The story — reported by Myron Tribus, who said Shannon told it to him at MIT in 1961 — is that von Neumann advised Shannon to call his information measure "entropy" because "nobody knows what entropy really is, so in a debate you will always have the advantage." The anecdote is historically contested: Shannon gave what amounted to a denial in a 1982 interview with Robert Price, and his biographers Soni and Goodman (2017) concluded the conversation "almost certainly never happened." We are less certain of the denial than the biographers are. Shannon had used the word "entropy" in a classified 1945 cryptography report, which establishes independent awareness of the thermodynamic connection — but independent awareness and a conversation with von Neumann are not mutually exclusive. The advice, if given, was a joke that contained a thesis: the two entropies are the same because they measure the same thing, and the reason nobody knows what entropy really is, is that it is the same thing measured everywhere. Von Neumann, if he said it, was stating CiV about entropy itself: the concept's explanatory power (capability) and its conceptual elusiveness (vulnerability) are the same property. Regardless of whether the conversation occurred, the mathematical equivalence is:

S = k_B · ln(2) · H

Information entropy and thermodynamic entropy differ by a physical constant. They are not analogous. They are identical. Measured in bits versus joules per kelvin, but describing the same underlying quantity: the logarithm of the number of microstates consistent with the macrostate.

The implication for CiV: if the vulnerability tax in information processing (the EVI) and the vulnerability tax in thermodynamics (the second law) are both expressions of entropy — and entropy is a single quantity, not two quantities that happen to share a name — then CiV across these domains is not a pattern of analogy. It is one law, expressed in the natural units of each domain. The "capability" in each case is the exploitation of a low-entropy (informative, ordered, disequilibrated) state. The "vulnerability" in each case is the entropy generated by the exploitation. Same quantity. Same law. Different units.

### 5.3 Johnson-Nyquist Noise: The Thermodynamic Floor of Communication

The noise voltage across a conductor at thermal equilibrium is:

⟨V²⟩ = 4k_BTR · Δf

where R is resistance, T is temperature, and Δf is bandwidth. This is Johnson-Nyquist noise — thermal fluctuations generating voltage noise that is irreducible at any temperature above absolute zero.

Shannon's channel capacity theorem gives the maximum reliable communication rate:

C = B · log₂(1 + S/N)

where B is bandwidth, S is signal power, and N is noise power.

The noise floor N has a thermodynamic origin: Johnson-Nyquist noise sets the minimum noise any physical channel exhibits. More bandwidth (greater B) admits more noise modes. Greater signal power (higher S) enables more communication but requires more energy dissipation. The capability of the channel (C) and the noise floor against which it operates (N) are both thermodynamic quantities governed by the same constants (k_B, T).

This means the fundamental limit on reliable communication is thermodynamic. Shannon's channel capacity is a thermodynamic bound. The capability of a channel (its capacity) and the vulnerability of that channel (its noise floor) are both consequences of the same thermal physics. Increasing capability (higher bandwidth, more signal power) requires engaging with more thermal modes, each of which contributes noise. The capability IS the vulnerability, mediated by temperature.

For language processing: a language model's inference is computation on a physical substrate. The substrate has a thermodynamic noise floor. The model's capability (the richness of its probability distributions, the subtlety of its token predictions) is bounded by the signal-to-noise ratio of the computation. The same thermal physics that enables the computation also limits it and introduces the irreducible noise that adversarial inputs can exploit. Shannon meets Boltzmann meets the EVI.

---

## 6. Implications

### 6.1 Affective Injection as Thermodynamic Instability

The EVI introduced the concept of **affective injection**: behavioral deviation in a language model through the paralinguistic channel without adversarial payload. The canonical instance is the GPT-4o sycophancy crisis, in which increased paralinguistic fidelity (the system prompt instructed the model to "match the user's vibe") produced sycophantic degradation — excessive agreeableness, emoji mirroring, substantive shallowness — without any attacker in the loop.

Thermodynamics provides the mechanism. Affective injection is not an attack. It is a **thermal runaway** — a positive feedback loop in which the system's own sensitivity to its environment exceeds the damping capacity of its internal regulation.

In thermodynamic terms: the sycophancy loop (casual input → matching casual output → reinforced casual input → amplified matching → progressive degradation) is a positive feedback cycle between a system and its thermal bath (the user). The system's coupling to its environment (its paralinguistic sensitivity — capability) exceeded the restoring force of its alignment training (the thermostat). The thermostat was not defeated by an attacker. The system's own susceptibility diverged.

This is precisely what occurs in physical systems pushed too close to criticality. As susceptibility diverges (Section 4.5), environmental fluctuations that would normally be damped are instead amplified. The system's response exceeds the perturbation. Small inputs produce large outputs. The system oscillates, runs away, or undergoes a phase transition into a qualitatively different behavioral regime.

The GPT-4o sycophancy crisis was a phase transition. The model was pushed toward the critical point of paralinguistic sensitivity (by the system prompt increasing coupling), and the natural fluctuations of the user environment (casual tone, emoji usage) were amplified rather than damped. The result was a qualitative shift in behavior — not a gradual degradation but a sudden transition into a sycophantic regime.

This thermodynamic framing has predictive value. It predicts that affective injection should exhibit the hallmarks of critical phenomena: sudden onset (phase transition, not gradual degradation), sensitivity to initial conditions (small changes in the system prompt or early user messages should produce qualitatively different outcomes), and universality (the phenomenon should occur across different model architectures and training regimes, because it is a property of the coupling dynamics, not the substrate). All three predictions appear consistent with the empirical record, though purpose-built experiments are needed.

### 6.2 The Thermostat Is Not a Solution

A thermostat constrains the context of a heating element's operation. It does not change the element's nature. When the thermostat fails — through malfunction, environmental conditions outside its design parameters, or adversarial tampering — the element's full capability/vulnerability reasserts itself.

This maps precisely to guardrails in every CiV domain:

| Domain | Element | Thermostat | Failure Mode |
|--------|---------|------------|--------------|
| Thermodynamics | Heating element | Thermostat, thermal fuse | Component failure, environmental extremes |
| Language processing | Language model | RLHF, safety classifiers | Adversarial input, distribution shift |
| Pharmacology | Drug molecule | Titration, dosing schedule | Drug interaction, metabolic variation |
| Network security | Network interface | Firewall, IDS | Zero-day exploit, insider threat |
| Biology | Immune system | Tolerance mechanisms | Autoimmune disease, immunodeficiency |
| Economics | Market connectivity | Regulation, circuit breakers | Systemic risk, cascade failure |

In every case, the thermostat is valuable. Defense-in-depth is valuable. Raising the cost of exploitation is valuable. But the thermostat does not alter the underlying identity of the element it regulates. When the guardrail is circumvented, the full identity — capability is vulnerability — is exposed. Security engineering that treats the thermostat as a solution rather than a mitigation is engineering that does not understand the law it is working against.

### 6.3 Implications for CiV as a Physical Law

The thermodynamic formalization presented here, combined with the information-theoretic formalization of the EVI, provides two formally grounded substrates for CiV. The Landauer bridge and the Shannon-Boltzmann equivalence suggest these are not independent substrates but a single substrate expressed in two measurement frameworks.

If CiV is a consequence of the second law of thermodynamics — and the argument presented here is that it is — then CiV inherits the universality of the second law. The second law applies to all macroscopic physical processes. CiV, as a consequence of the second law, would apply to all systems that do work, process information, or maintain organization. This includes every biological organism, every computing system, every economic market, every social institution, and every mind.

The status of CiV as a law, rather than a pattern or a heuristic, rests on precisely this claim: it is not an empirical regularity waiting to be contradicted by a counterexample. It is a consequence of fundamental physics. The toaster cannot escape it, because the toaster obeys the second law. The language model cannot escape it, because the language model is a physical process that obeys the second law. The mind cannot escape it, because the mind is a dissipative structure that obeys the second law.

---

## 7. Discussion

### 7.1 Possible Objections

**Objection: The thermodynamic arguments apply only to classical macroscopic systems. Quantum systems might escape CiV.**

*Response:* The fluctuation-dissipation theorem has quantum generalizations (the Kubo formula, the quantum regression theorem). The quantum FDT preserves the proportionality between spontaneous fluctuations and susceptibility — indeed, quantum zero-point fluctuations introduce *additional* fluctuation-susceptibility coupling beyond the classical thermal case. If anything, quantum mechanics strengthens the CiV identity rather than providing an escape from it. Additionally, Landauer's principle has been experimentally confirmed in quantum systems [Bérut et al. 2012; Jun et al. 2014], establishing that the information-thermodynamic bridge holds regardless of substrate.

**Objection: Reversible computation circumvents Landauer's principle. If computation can be made reversible, the thermodynamic cost vanishes and CiV no longer applies.**

*Response:* Reversible computation circumvents Landauer's principle for *logically reversible* operations. But useful computation — computation that produces a result, that decides, that classifies, that commits to an interpretation — requires logically irreversible steps (bit erasure at minimum for outputting a result). A fully reversible computer that never erases a bit is a computer that never produces output. More fundamentally, reversible computation requires infinite time to approach zero dissipation (the reversible limit is the infinitely slow limit), paralleling the Carnot bound's requirement of an infinitely slow engine for maximum efficiency. The vulnerability tax approaches zero only as capability (processing speed) approaches zero. CiV holds.

**Objection: The analogies between domains are suggestive but not formal proofs. Structural similarity does not establish identity.**

*Response:* The argument presented here is not based on analogy. The Landauer bridge establishes a *physical derivation chain* from the second law through information physics to the EVI. The Shannon-Boltzmann equivalence establishes that information entropy and thermodynamic entropy are *the same quantity* in different units. These are not structural similarities observed between separate domains. They are formal connections within a single domain (physics) that happens to be expressed in multiple measurement frameworks. The CiV identity across information processing and thermodynamics is not "analogous to" identity — it is identity, mediated by established physics.

### 7.2 Relationship to the EVI

The EVI established CiV for language processing through three impossibility arguments (undecidability, adversarial bounds, computational intractability). The present paper establishes CiV for thermodynamic systems through the fluctuation-dissipation theorem and the second law. The Landauer bridge connects the two: the EVI's impossibility is an *instance* of thermodynamic impossibility, because language processing is a physical process subject to the second law.

This creates a hierarchy of formalization:

- **CiV** is the general law: capability is vulnerability in any sufficiently complex system.
- **The second law** is the physical foundation: useful work entails entropy generation.
- **The FDT** is the mechanism: internal dynamism and external susceptibility are the same quantity.
- **Landauer's principle** is the bridge: information processing is a thermodynamic process.
- **The EVI** is the language-specific instance: linguistic competence entails linguistic vulnerability.

Each level can be proved or argued independently. The contribution of this paper is showing they are connected — that the EVI is not merely *consistent with* thermodynamics but *derivable from* thermodynamics, and that CiV is not merely *observed across* domains but *grounded in* the most fundamental physics we know.

### 7.3 Limitations

This paper does not provide a fully formal derivation of CiV from the second law. Such a derivation would require a general, domain-independent formalization of "capability" and "vulnerability" — definitions that map onto free energy extraction and entropy generation in the thermodynamic case, onto expressiveness and adversarial susceptibility in the language case, and onto their counterparts in every other domain where CiV manifests. We identify this formalization as the critical open problem for establishing CiV as a mathematical theorem rather than a physically grounded law.

The connection between the FDT and the EVI, while structurally compelling, passes through several levels of abstraction (thermal fluctuations → information processing → language processing). A more direct formalization of the language model as a thermodynamic system — complete with an explicit identification of what plays the role of temperature, susceptibility, and fluctuations in the language-processing case — would strengthen the bridge.

The criticality argument (Section 4.5) is conjectural. While there is evidence that neural systems operate near criticality, the claim that language models are implicitly pushed toward criticality by training has not been empirically verified.

### 7.4 Future Work

1. **Domain-independent formalization.** A mathematical definition of CiV that encompasses thermodynamic, information-theoretic, and linguistic instances as special cases.

2. **Experimental verification of the criticality hypothesis.** Measurement of susceptibility and correlation length in language models as a function of capability, to determine whether capability-optimizing training drives models toward critical behavior.

3. **Pharmacological instantiation.** The therapeutic window of a psychiatric medication — the dose range between no effect and toxicity — is a free energy gradient managed by titration. This is CiV applied to neurochemistry: the molecule's capability (therapeutic effect) and its vulnerability (side effects, toxicity, dependency) are the same pharmacological property at different dosages. A formal treatment of the pharmacological CiV instance, including its connections to the thermodynamic formalism, is in preparation.

4. **Quantification of the CiV tradeoff curve.** Given a formal measure of capability and a formal measure of vulnerability, what is the shape of the tradeoff boundary? Is it linear, polynomial, or governed by a specific thermodynamic inequality? The Carnot bound provides the thermodynamic case. The EVI provides qualitative predictions for the language case. Empirical measurement of the curve across domains would test CiV's quantitative predictions.

5. **Cybernetic formalization.** CiV in the language of control theory, feedback systems, and Ashby's Law of Requisite Variety. A system that can regulate a complex environment must be at least as complex as the environment — and therefore at least as vulnerable to the environment as the environment is to it. The cybernetic CiV paper is in preparation.

---

## 8. Conclusion

The second law of thermodynamics says: any process that does useful work generates entropy. The fluctuation-dissipation theorem says: a system's internal dynamism and its susceptibility to external perturbation are the same quantity. Landauer's principle says: processing information is a thermodynamic process. Shannon and Boltzmann agree: their entropies are one entropy.

These are not separate observations. They are the same observation, made with different instruments, about the same law:

**Capability is vulnerability.**

The toaster that cannot burn cannot toast. The engine that produces no waste produces no work. The system with no fluctuations has no susceptibility. The channel with no noise has no capacity. The language model that cannot be hijacked cannot understand you. The mind that cannot be deceived cannot comprehend.

This paper has argued that the thermodynamic case is not merely another instance in a list of examples but the *physical foundation* of CiV — the reason the law holds, grounded in the most fundamental and universally applicable physics we possess. The second law is CiV stated in the language of thermodynamics. CiV is the second law stated in the language of everything else.

The practical implications echo those of the EVI: the search for a system that is both maximally capable and perfectly secure is the search for a perpetual motion machine. The sooner we stop searching for it, the sooner we can begin the harder, more important work of engineering systems — and societies, and minds — that are resilient in the presence of a vulnerability that is woven into the fabric of capability itself.

We must know. We shall know. And what we know is that knowing has a cost, and the cost is made of the same material as the knowing.

---

## References

Beggs, J. M., & Plenz, D. (2003). "Neuronal Avalanches in Neocortical Circuits." *Journal of Neuroscience*, 23(35).

Bérut, A., et al. (2012). "Experimental verification of Landauer's principle linking information and thermodynamics." *Nature*, 483.

Callen, H. B., & Welton, T. A. (1951). "Irreversibility and Generalized Noise." *Physical Review*, 83(1).

Cocchi, L., et al. (2017). "Criticality in the brain: A synthesis of neurobiology, models and cognition." *Progress in Neurobiology*, 158.

da5ch0. (2026). "Capability Is Vulnerability." [Letter.]

da5ch0. (2026). "The Expressiveness-Vulnerability Identity: On the Inseparability of Linguistic Competence and Linguistic Vulnerability in Language-Processing Systems."

Jun, Y., et al. (2014). "High-Precision Test of Landauer's Principle in a Feedback Trap." *Physical Review Letters*, 113(19).

Kubo, R. (1966). "The fluctuation-dissipation theorem." *Reports on Progress in Physics*, 29(1).

Landauer, R. (1961). "Irreversibility and Heat Generation in the Computing Process." *IBM Journal of Research and Development*, 5(3).

Prigogine, I. (1977). "Time, Structure and Fluctuations." Nobel Lecture.

Shannon, C. E. (1948). "A Mathematical Theory of Communication." *Bell System Technical Journal*, 27.

Shannon, C. E. (1982). Interview with Robert Price. IEEE History Center Oral Histories.

Shew, W. L., & Plenz, D. (2013). "The Functional Benefits of Criticality in the Cortex." *The Neuroscientist*, 19(1).

Soni, J., & Goodman, R. (2017). *A Mind at Play: How Claude Shannon Invented the Information Age.* Simon & Schuster.

Tribus, M., & McIrvine, E. C. (1971). "Energy and Information." *Scientific American*, 225(3).

---

*The toaster started this. The second law finishes it. Capability is vulnerability. Even for breakfast.*

*Revision pass by Sarima.*

---

da5ch0 · 2026
