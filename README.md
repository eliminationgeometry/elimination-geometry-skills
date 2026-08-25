# Elimination Geometry Research and Engineering Tools

**English** | [简体中文](README_CN.md)

> Cross-disciplinary research and engineering tools for applying **Elimination Geometry (EG)** across mathematics and optimization, information and computational sciences, artificial intelligence and statistics, control and decision sciences, engineering, quantum and physical sciences, economics, and life, health, and Earth systems.

**Book preprint:** [Elimination Geometry — arXiv:2608.17646](https://arxiv.org/abs/2608.17646)

## What is Elimination Geometry?

In many problems, there is a structural gap between local solvability and global realizability. Even when every local problem can be solved optimally on its own, there may be no single shared, deployable mechanism that realizes all of those local optima at once. Elimination Geometry studies precisely this divide between being **locally solvable** and being **globally deployable**.

Suppose an auxiliary object \(a\) is optimized out of a local objective:

$$
J(x)=\inf_{a\in\mathcal A} H_x(a).
$$

Inserting a non-oracle object back into the original problem creates the native defect

$$
D_x(a)=H_x(a)-J(x)\ge 0.
$$

This is not an arbitrary distance chosen after the fact. It is the exact excess cost measured in the native units of the original objective: likelihood, divergence, proper score, energy, regret, Bellman loss, free energy, or another declared criterion.

The central distinction is

$$
\forall x\;\exists a_x^\star
\qquad\not\Rightarrow\qquad
\exists A\in\mathfrak A\;\forall x,
\quad A(x)\approx a_x^\star.
$$

Every local problem may have a good solution, while no single rule in the admissible deployment class \(\mathfrak A\) can realize all of them simultaneously. The obstruction may come from shared parameters, limited memory, continuity, a fixed representation, communication constraints, computational limits, or another architectural contract.

EG organizes this problem into three levels:

1. **Local solvability:** What is the pointwise oracle, and what does deviation from it cost?
2. **Global realizability:** Can one admissible shared mechanism realize the local oracle field?
3. **Finite-sample certifiability:** Can available data distinguish realizability, nonrealizability, and an unresolved case with controlled error?

It also keeps four sources of failure separate: local-model approximation, architecture obstruction, finite-sample generalization, and implementation or optimization error. Moving from a mathematical obstruction to a scientific or engineering intervention requires additional transmission, task-exposure, saturation, and validation arguments.

## What is included?

This repository contains four independent, self-contained skills.

### `eg-library`

A source-grounded library companion for the EG monograph and the 33-paper research corpus. It is designed for:

- definitions, formulas, theorem and proof lookup;
- assumption and claim-boundary verification;
- paper and book routing;
- cross-source synthesis, provenance, and citation;
- exact rereading of the relevant primary manuscript when precision matters.

### `eg-research-collaborator`

A research-development companion for turning an unfamiliar domain problem into a rigorous and falsifiable EG research program. It supports:

- problem translation and formulation audits;
- theorem, counterexample, and certificate design;
- novelty and prior-art analysis;
- experiment contracts and mechanism-matched interventions;
- manuscript organization and adversarial referee review.

### `eg-engineering-analysis`

A scientific and physical-engineering companion for analyzing, modeling, designing, optimizing, and verifying engineered systems. It supports:

- governing equations, units, geometry, materials, boundary and loading conditions;
- reduced-order and surrogate models, closures, controls, sensing, and simulation;
- materials and microstructure, structures, fluids, waves, optics, acoustics, electromagnetics, process, energy, and Earth systems;
- model-form, representation, parameter, numerical, implementation, and experimental error separation;
- physical witnesses, uncertainty analysis, mechanism-matched interventions, and independent validation.

### `eg-software-engineering`

A repository-grounded companion for designing, diagnosing, implementing, optimizing, and verifying software systems. It supports:

- software architecture, integration, APIs, schemas, caches, and state machines;
- distributed and streaming systems, data and ML infrastructure, numerical software, and deployment;
- correctness, performance, reliability, compatibility, security boundaries, and resource analysis;
- executable witnesses, discriminating tests, minimal code or contract changes, and layered verification.

The two engineering skills are routed by the **dominant artifact and acceptance contract**, not by the application label. A fluid simulation is an engineering-analysis task when the question is closure, boundary conditions, or physical validity; it is a software-engineering task when the question is solver implementation, concurrency, memory, or runtime behavior. Cyber-physical and scientific-computing work can use either boundary explicitly without forcing one skill to load the other.

## Why does EG work?

EG is effective not because it forces different disciplines into one formula, or because abstract language can replace domain knowledge and rigorous proof. It changes how a research problem is represented, in what order inferences are made, and which actions the evidence permits: identify the eliminated local oracle and its native cost; declare the sharing and deployment contract; preserve the order of noncommuting operations; record different failures in different ledgers; and allow each kind of evidence to authorize only a matching conclusion and intervention.

### 1. Typed ledgers: prevent one problem from masquerading as another

EG first derives an exact native defect from the original problem: the excess cost, in likelihood, risk, energy, regret, or another native unit, of inserting a non-oracle object back into the criterion. It then separates quantities often grouped under the words “error,” “information,” or “complexity” into different ledgers: native objective, architecture capacity, operational semantics, statistical evidence, recursive state, and implementation or optimization. Each ledger has its own objects, units, and quantifiers.

The ledgers also preserve operation order. Eliminating pointwise and then imposing sharing is generally a different problem from imposing a shared constraint before elimination:

$$
\mathrm{Eliminate}\circ\mathrm{Couple}
\neq
\mathrm{Couple}\circ\mathrm{Eliminate}.
$$

Compression can likewise merge distinctions needed for deployment, certification, or future updates. EG's **no-compensation principle** does not say that resources can never be exchanged. It says that, without an explicit exchange theorem, quantities from different ledgers may not be added, substituted, or used to cancel one another. More data do not automatically remove an architecture obstruction; a larger deployment model cannot reconstruct likelihood directions erased by the evidence interface; and better optimization cannot create distinctions absent from the representation. Typed accounting therefore prevents category errors, false causal diagnoses, and irrelevant interventions.

### 2. Certification and action: know when to conclude and what to do next

EG does more than analyze structural obstructions. It connects finite-data decisions, system-capacity limits, and the choice of the next intervention into a certification–action system. A confidence world retains every complete world compatible with the available data. The system reports “certified feasible” or “certified impossible” only when those worlds agree; otherwise it honestly reports “unresolved.” Even if every compatible world admits some feasible architecture of its own, there may still be no single architecture that is safe to deploy across all of them now.

EG also distinguishes three carriers that are not interchangeable by default. A deployment carrier preserves the oracle distinctions needed to act; an evidence carrier preserves the statistical distinctions needed to authorize a conclusion; and a recursive carrier preserves the state distinctions needed to choose future observations and continue updating. A failure witness therefore routes to a matching action: change the scientific model for local-model failure; change the sensor, statistic, or experiment for evidence blindness; split state or add memory for a recursive collision; change representation, routing, atlases, or decoders for a deployment collision; and spend more optimization or compute only when an admitted solution has merely not been reached.

The result is an auditable responsibility chain:

$$
\text{local oracle}
\longrightarrow
\text{native defect}
\longrightarrow
\text{sharing or compression constraint}
\longrightarrow
\text{collision and obstruction}
\longrightarrow
\text{transmission and task exposure}
\longrightarrow
\text{confidence certification}
\longrightarrow
\text{matched action}.
$$

EG therefore asks not only “Why did this fail?” but also “What is currently known?”, “Which kind of evidence or capacity is still missing?”, and “What is the most informative next action?”

### 3. A heuristic engine: turn open problems into structured search

EG supplies reusable research heuristics: seek the smallest noncommuting elimination–coupling square; change quantifier order and test the gap between pointwise and common existence; find the smallest pair of oracles merged by a shared carrier; derive the defect from the original objective rather than choosing an arbitrary distance; check whether an internal defect reaches and is exposed by the declared task; search boundaries, singularities, topology, dependence, products, and tensorization for counterexamples; and let a failed conjecture identify a sharper, testable successor.

These heuristics do not guarantee novelty or replace proof. They narrow the search space, rule out interventions unrelated to the diagnosed obstruction, and organize exploration into a cycle of structural conjecture, minimal witness, transmission test, certificate, and repair. The counterexample cascade in the Marton case below is one representative instance of this discovery mechanism.

### 4. An executable research graph: make dispersed knowledge work together

A foundation model may separately know about EM, Bregman distances, Schur complements, missing information, rate–distortion, topological obstructions, and confidence sets. Yet these ideas live in different papers, disciplines, and contexts. After pretraining compresses a vast corpus into model parameters, the individual facts may remain while their cross-disciplinary links fail to be retrieved, ordered, and activated together for a new problem. The knowledge has not literally been deleted; the relevant relations may simply be weak links without a stable path of use.

EG organizes these dispersed ideas into a typed, evidence-bearing, action-linked **executable research graph**. It records not only which concepts exist, but which object came from which elimination, which defect uses which native unit, which carrier must preserve which distinction, which gate permits which inference, and which failure witness should trigger which action. EM and Bregman distance, for example, become parts of one reasoning chain through variational elimination, exact insertion defects, conditional projection, and local convergence structure rather than two isolated entries.

The repository's four EG skills deploy this organization for different tasks: `eg-library` handles primary-source retrieval, verification, and synthesis; `eg-research-collaborator` develops unfamiliar problems into falsifiable research programs; `eg-engineering-analysis` serves physical, scientific, and multidisciplinary engineered systems; and `eg-software-engineering` serves code, software architecture, and runtime systems. Each uses a compact canon to preserve core relations and reasoning order, keeps the complete monograph and papers as traceable external memory, and rereads exact sources on demand for the problem at hand.

What EG gives an AI first is not more facts, but types, adjacency, retrieval order, evidence thresholds, and next actions among the facts it already has. It helps dispersed knowledge work together on the right problem and in the right order.

## Representative cases

### (1) Marton's inner bound is strictly suboptimal

**Mian Huang, Yanxiao Liu, and Yi Liu**,  
*Sub-optimality of Marton's Inner Bound for the Two-Receiver Broadcast Channel*  
[[arXiv abstract](https://arxiv.org/abs/2608.19869)] [[PDF](https://arxiv.org/pdf/2608.19869)]

Introduced in 1979, Marton's inner bound remained the best-known achievable region for the general two-receiver discrete memoryless broadcast channel. This work proves that it does not always reach the capacity region, resolving a longstanding optimality question.

The paper records EG's concrete role in the collaborative discovery process: AI-assisted structural search progressed from a counterexample to a Markovity conjecture through tensorization and additivity to a counterexample to Marton optimality, after which rigorous mathematics completed the proof. It is a successful example of EG moving from structural diagnosis to an important theoretical discovery.

### (2) The Data Selection problem

**Mian Huang**  
*Exact Data Selection: Low Dimensions and Budget Two*  
[[Paper and DOI](https://doi.org/10.5281/zenodo.21712106)] [[COLT 2025 open problem](https://proceedings.mlr.press/v291/hanneke25e.html)]

When a learning algorithm is fixed and may retain only a small subset of a full dataset, which samples best preserve full-data performance? This work treats the selection budget as a resource coordinate and the excess squared loss of the selected-sample mean relative to the full-data mean as the native defect. It solves the low-dimensional mean-estimation case exactly and identifies the dimension-dependent transition at budget two. EG's role is to view the selected samples as a budget-limited information carrier and price data compression directly in the original squared loss, producing a clear “how much data versus how much performance” frontier.

### (3) Data analysis in quantum computing: “Correct on average” does not mean “reliable”

In quantum computing and quantum information, a quantum state cannot be read out in full like ordinary data. Researchers must aggregate many randomized measurements to estimate global properties such as quantum entropy. Even if every local estimator is unbiased, this says only that its long-run average is correct; it does not guarantee small fluctuations with finite data. Different aggregation rules can be equally unbiased while retaining very different high-order noise. **Correct local components do not guarantee a correct shared aggregation mechanism.**

EG audits the **estimation object**, **aggregation architecture**, and **final risk** separately: expose the aggregation bottleneck in a minimal case, prove its actual cost, and then apply a matched repair such as using a more complete set of sample combinations. The same obstruction–witness–repair route applies to batches, subgraphs, expert outputs, and distributed computation, while preventing local correctness from being overstated as a broad global guarantee.

## A cross-disciplinary research map

The same local-to-global structure appears under different names across science and engineering. The map below is deliberately broad, but it must be read with an important distinction:

- An **established EG foundation** means that the current monograph or 33-paper collection contains an explicit EG formulation, theorem, calibration, worked example, or research development in at least part of that area.
- An **EG direction for further development** means that the area contains promising elimination-and-deployment problems, but a genuine EG result still requires a domain-correct objective, an exact elimination identity, an admissible shared architecture, and new mathematics or evidence. Inclusion in this map is not a claim that such a result has already been proved.

### Mathematics and foundational methods

- **Convex and variational analysis — established EG foundation:** Legendre duality, Bregman defects, partial minimization, saddle elimination, convex–concave structure, proximal constructions, variational inequalities, strong convexity, and stability of argmin maps.
- **Geometry, topology, and singularity theory — established EG foundation:** fibers and quotients, bundles and atlases, monodromy, discriminants, degree, stratification, catastrophe taxes, integrability, Hodge repair, and topological obstructions to a continuous global choice.
- **Graph theory and network mathematics — established EG foundation:** graph-indexed distributions, graph smoothing, flow duality, cuts and cycles, holonomy, message transmission, network quotients, and graph-constrained deployment.
- **Combinatorics and discrete mathematics — EG direction for further development:** finite set systems, matroids, matchings, colorings, constraint-satisfaction problems, discrete Morse structures, combinatorial topology, and local witnesses that cannot be assembled into one global feasible object.
- **Discrete and combinatorial optimization — EG direction for further development:** mixed-integer optimization, polyhedral and conic lifts, integrality gaps, decomposition, scheduling, routing, facility location, branch-and-bound state, and resource-constrained approximation.
- **Functional, operator, and spectral analysis — established EG foundation:** eigenvectors and eigenspaces, spectral branches, operator-valued elimination, invariant subspaces, Schur complements, approximate spectral certificates, and matrix-free deflation.
- **Differential equations and dynamical systems — partly established, partly to be developed:** ordinary, partial, stochastic, and differential-algebraic equations; closure, multiscale reduction, homogenization, singular perturbation, bifurcation, stability, inertial manifolds, and reduced-order dynamics. Mori–Zwanzig closure and multiscale dynamics are established EG foundations; the wider PDE program is a direction for further EG development.
- **Numerical analysis and scientific computing — partly established, partly to be developed:** surrogate and reduced-order models, iterative solvers, preconditioning, deflation, adaptive discretization, multigrid, domain decomposition, operator compression, error certification, and structure-preserving approximation. Exactification and certified deflation have an established EG foundation.

### Statistics, machine learning, and artificial intelligence

- **Mathematical statistics — established EG foundation:** likelihood and profile elimination, latent-variable models, EM, estimating equations, proper scores, confidence sets, partial identification, model conflict, finite-sample certificates, and resolution complexity.
- **Bayesian and computational statistics — established EG foundation:** variational inference, posterior compression, amortized inference, nuisance elimination, approximate inner solutions, Monte Carlo surrogates, and the separation of posterior guidance from frequentist certification.
- **Time-series, spatial, and dependent-data statistics — established EG foundation:** dependence-aware defects, long-memory forecasting, state compression, change of scale, graph-indexed observations, and recursive sufficiency.
- **Causal inference and experimental design — EG direction for further development:** nuisance adjustment, mediator or latent-state elimination, transport across environments, task-specific identification, adaptive acquisition, sequential experiments, and certificates for interventions chosen under uncertainty.
- **Machine learning — established EG foundation:** representation learning, multitask learning, meta-learning, amortized prediction, graph learning, generative and latent-variable models, model compression, distillation, architecture comparison, and obstruction-aware learning.
- **Deep learning systems — partly established, partly to be developed:** shared encoders, mixture-of-experts routing, neural operators, recurrent and memory architectures, attention bottlenecks, conditional computation, low-rank adaptation, and deployment under compute or communication limits. The architectural audit has an established EG foundation; model-family-specific theorems remain directions for further EG development.
- **Artificial intelligence and agent systems — EG direction for further development:** planning, search, tool use, world models, retrieval, long-horizon memory, multi-agent coordination, neuro-symbolic systems, reusable reasoning modules, and the distinction between current-task sufficiency and recursive closure.
- **Reinforcement learning and sequential learning — partly established, partly to be developed:** policies, value functions, Bellman elimination, state abstraction, partial observability, offline-to-online transfer, exploration, regret, and adaptive structural expansion. Shared-policy and recursive-state questions have an established EG foundation.
- **Scientific machine learning — EG direction for further development:** physics-informed learning, learned closure, operator learning, surrogate simulation, inverse problems, reduced-order discovery, and digital twins whose shared representations must preserve task-visible fine-scale structure.

### Information, computation, and security

- **Information theory — established EG foundation:** rate–distortion, information radius, task-relevant compression, certificate information bottlenecks, data processing, worldwise KL separation, communication–sample tradeoffs, and recursive rate–distortion.
- **Coding and communication theory — partly established, partly to be developed:** source and channel coding, distributed coding, finite-blocklength reliability, feedback, semantic communication, network information flow, causal coding, and task-dependent decoders. Several information and certificate interfaces have an established EG foundation; full coding theorems are direction-specific.
- **Signal processing and imaging — partly established, partly to be developed:** sampling, wavelets, compressed sensing, denoising, inverse imaging, sensor fusion, spectral estimation, adaptive acquisition, and task-visible compression. Certificate-directed wavelet acquisition has an established EG foundation.
- **Theoretical computer science — EG direction for further development:** algorithms and complexity, streaming and sketching, online algorithms, communication complexity, approximation algorithms, data structures, distributed computation, and resource lower bounds derived from lost oracle distinctions.
- **Programming languages and formal methods — partly established, partly to be developed:** operational semantics, contextual equivalence, abstract interpretation, program refinement, compiler passes, proof-carrying transformations, model checking, and compositional verification. Context-safe replacement and operational observability are established EG foundations.
- **Databases and distributed systems — EG direction for further development:** query planning, view selection, data integration, consistency models, caching, replicated state, distributed summaries, and when a local query-optimal representation cannot be deployed as one shared schema or protocol.
- **Cryptography, privacy, and security — EG direction for further development:** cryptographic protocols, secure multiparty computation, zero knowledge, secret sharing, differential privacy, privacy-preserving learning, adversarial robustness, leakage channels, and cyber-physical security. EG would require a precise security/task defect and cannot infer cryptographic security from information loss alone.

### Decisions, control, games, and economic systems

- **Control theory — established EG foundation:** stochastic and robust control, entropy-regularized control, control as inference, state estimation, finite-memory control, model predictive control, system identification, and the transmission of local model defects into closed-loop loss.
- **Robotics and autonomous systems — EG direction for further development:** perception–control compression, localization and mapping, motion planning, manipulation, multi-robot coordination, embodied memory, safety filters, and deployable policies under sensing and compute limits.
- **Game theory and strategic learning — established EG foundation:** strategic regret, best-response or equilibrium objects, repeated and stochastic games, learning in games, information-limited play, recursive strategic state, and multi-agent coordination.
- **Economics and econometrics — partly established, partly to be developed:** structural and dynamic models, latent heterogeneity, sufficient-state reduction, mechanism design, market design, industrial organization, matching, dynamic discrete choice, and policy deployment across heterogeneous agents. Strategic and statistical interfaces have an established EG foundation; domain-specific identification remains to be established.
- **Finance and market design — partial EG research foundation:** market microstructure, limit-order-book event order, execution-visible states, information compression, portfolio or risk-state aggregation, algorithmic execution, and sequential decision-making under operational constraints.
- **Operations research and service systems — partial EG research foundation:** queueing, state-space collapse, scheduling, inventory, supply chains, transportation, logistics, revenue management, and resource allocation. Task-visible queueing reductions have an established EG foundation.

### Quantum and physical sciences

- **Quantum mechanics — established EG foundation:** density operators, quantum relative entropy, noncommutative state elimination, measurement-dependent visibility, spectral subspaces, and the difference between classical and quantum realizability.
- **Quantum information and quantum computing — partly established, partly to be developed:** quantum channels, measurements, state compression, entanglement-sensitive representations, quantum control, variational quantum algorithms, tensor-network truncation, quantum error correction, and compilation under restricted gate or measurement architectures. Noncommutative rigidity has an established EG foundation; most algorithmic applications remain directions for further EG development.
- **Statistical physics and thermodynamics — established EG foundation:** free-energy defects, coarse-graining, renormalization, entropy production, nonequilibrium paths, diffusion, hidden dissipation, and task-conditioned macrostates.
- **Complex systems and interacting particles — EG direction for further development:** kinetic limits, collective behavior, spin systems, disordered systems, phase transitions, emergent macrostates, agent-based models, and task-relative coarse variables.
- **Classical and continuum mechanics — EG direction for further development:** elasticity, plasticity, fracture, contact, multibody systems, constitutive reduction, finite-element model reduction, and elimination of unresolved internal variables.
- **Fluid mechanics — EG direction for further development:** turbulence and closure, large-eddy simulation, multiphase and reacting flows, boundary layers, geophysical fluids, flow control, data assimilation, and reduced-order models that must retain task-visible coherent structures.
- **Wave physics, optics, and acoustics — EG direction for further development:** wave propagation, geometrical and wave optics, photonics, diffraction, inverse scattering, computational imaging, acoustics, aeroacoustics, vibration, seismology, and reduced representations constrained by phase, polarization, coherence, or boundary data.
- **Electromagnetism and plasma physics — EG direction for further development:** Maxwell solvers, antenna and inverse design, electromagnetic scattering, plasma closure, kinetic-to-fluid reduction, reduced-order field models, and multiscale coupling.
- **Chemistry and molecular science — EG direction for further development:** reaction networks, chemical kinetics, molecular dynamics, electronic-structure reduction, free-energy surfaces, coarse-grained molecular models, catalysis, and uncertainty-aware reaction-state compression.

### Engineering and designed materials

- **Composite materials and microstructure — EG direction for further development:** microstructure-to-property maps, representative volume elements, homogenization, multiscale constitutive laws, damage and failure, process–structure–property links, and whether one reduced material descriptor can serve all loading paths and tasks.
- **Metamaterials and architected media — EG direction for further development:** mechanical, acoustic, photonic, and electromagnetic metamaterials; topology optimization; band-structure design; multiscale resonances; and task-specific effective parameters.
- **Structural, civil, and geotechnical engineering — EG direction for further development:** structural health monitoring, reduced structural models, reliability, earthquake engineering, soil–structure interaction, porous media, and sensor-limited damage localization.
- **Mechanical, aerospace, and automotive engineering — EG direction for further development:** aerodynamic and structural design, propulsion, combustion, thermal management, guidance and navigation, fault diagnosis, digital twins, and certification under shared onboard resources.
- **Electrical and electronic engineering — partly established, partly to be developed:** circuits, communication systems, estimation, control, power electronics, sensor networks, chip design, hardware-aware AI, and signal representations constrained by bandwidth, energy, latency, or precision.
- **Chemical and process engineering — EG direction for further development:** process control, reactor networks, separation, multiscale transport, reduced kinetics, process monitoring, fault diagnosis, and deployment across operating regimes.
- **Manufacturing and design engineering — EG direction for further development:** topology and multidisciplinary design optimization, additive manufacturing, process planning, quality control, surrogate-based design, and transferable digital twins.
- **Energy systems — EG direction for further development:** power grids, batteries, electrochemical systems, renewable integration, energy markets, demand response, storage control, and cross-scale models linking material state to system operation.

### Life, health, Earth, and environmental systems

- **Systems and computational biology — EG direction for further development:** gene regulation, signaling and metabolic networks, population dynamics, phylogenetics, molecular coarse-graining, cell-state representations, and multiscale biological models.
- **Neuroscience — EG direction for further development:** neural population codes, latent-state models, dynamical systems, connectomics, task-dependent neural compression, brain–computer interfaces, and representations that must remain sufficient under future updates.
- **Medicine and public health — EG direction for further development:** medical imaging, clinical prediction, personalized treatment, pharmacometrics, physiological digital twins, epidemiology, adaptive trials, and deployment across heterogeneous populations and institutions.
- **Earth, climate, and environmental science — EG direction for further development:** atmosphere–ocean models, climate parameterization, hydrology, subsurface flow, remote sensing, seismic inversion, weather prediction, ecosystem models, and cross-scale uncertainty propagation.
- **Infrastructure and networked systems — partly established, partly to be developed:** transportation, communication networks, cloud and edge systems, smart cities, water networks, supply networks, resilience, cascading failures, and distributed decision-making. Queueing and operational-state examples have an established EG foundation.

EG does not replace the established theories in any of these fields. Its proposed role is narrower: provide a common, typed interface for asking which distinctions survive elimination, which are lost by a shared deployment contract, how the loss is priced in native units, whether it reaches the declared task, whether finite data can certify it, and what structural repair is justified.

### When does a new application genuinely become EG?

A subject is not an EG application merely because it contains latent variables, reduction, compression, or a residual. A defensible formulation must identify:

1. the exact object being eliminated and the admissible local oracle;
2. an insertion identity producing a nonnegative native defect;
3. the shared architecture, resource, representation, or deployment contract;
4. the quantifiers—pointwise or common, average or worst case, fixed or adaptive;
5. the transmission path and task exposure needed to convert native defect into downstream consequence;
6. the finite-information certificate, or an explicit statement that the question remains statistically unresolved;
7. a saturation test and mechanism-matched repair before recommending an intervention.

## Research corpus

All four skills contain the complete Version 1.9 monograph source snapshot, the **Core16** manuscripts, and the **Extend17** domain extensions. Each is independent and does not call another EG skill. They initialize a compact role-specific memory and reread exact chapters or papers on demand. They do not treat a summary, search hit, analogy, numerical failure, or engineering proxy as a substitute for the underlying source or evidence.

- **Core16** develops the common EG framework: certified elimination, native defects, the P/G/X/V/C design split, integrability and representation gates, composition, transfer, operational semantics, statistical certificates, architecture ledgers, adaptive learning, and exactification-based optimization.
- **Extend17** develops domain-facing research in information theory, strategic learning, time series and dynamical closure, statistical physics and renormalization, queueing, and market microstructure.

The distinction between *core* and *extension* describes logical role, not importance. Historical priority should be assessed at the level of the full problem contract and theorem chain: an inherited component formula must be credited, but a formula match alone does not establish identity of the surrounding framework.

## Example questions

- What is the correct eliminated auxiliary object and native defect for a new scientific problem?
- Does a proposed architecture face a genuine realizability obstruction, or only an optimization failure?
- Which theorem assumptions are needed to transport a native defect into downstream task loss?
- Can finite data certify the obstruction, or must the answer remain unresolved?
- Which Core16 or Extend17 sources should be read for a particular domain?
- Is a proposed contribution mathematically new, a specialization, an integrated synthesis, or an analogy?
- Why do locally correct modules fail after integration through one shared state or interface?
- Is a software performance gap caused by architecture, workload evidence, algorithm, implementation, protocol, or resource limits?
- What is the smallest mechanism-matched code or contract change, and which tests and benchmarks should verify it?
- Is a simulation discrepancy caused by governing physics, shared closure, parameters, discretization, implementation, or experimental mismatch?
- Which physical state, mode, load path, or operating regime should be retained, sensed, or tested before redesign?

## Canonical reference

Mian Huang and Xueqin Wang. “Elimination Geometry.” *arXiv:2608.17646* [cs.LG], 2026.  
<https://arxiv.org/abs/2608.17646>

```bibtex
@misc{HuangWang2026EliminationGeometry,
  title         = {Elimination Geometry},
  author        = {Mian Huang and Xueqin Wang},
  year          = {2026},
  eprint        = {2608.17646},
  archivePrefix = {arXiv},
  primaryClass  = {cs.LG},
  url           = {https://arxiv.org/abs/2608.17646}
}
```

## Contact

For research collaboration, technical questions, corrections, and commercial licensing inquiries, contact:

> **Elimination Geometry Project**  
> [eliminationgeometry@gmail.com](mailto:eliminationgeometry@gmail.com)

This project address is the official public contact for the repository. Commercial authorization requires a separate written agreement from the applicable rights holders; an email inquiry does not itself grant permission.

## License and use

The package is **source-available for noncommercial research**; it is not presented as OSI-approved open-source software.

- Original EG research content and skill documentation are offered under **CC BY-NC-SA 4.0**, unless a file states otherwise.
- Original maintenance scripts are offered under the **PolyForm Noncommercial License 1.0.0**.
- Bundled manuscripts, bibliographies, figures, data, and third-party materials retain their own applicable terms.
- Commercial use requires a separate written license from Mian Huang and any other applicable rights holder.

See the `LICENSE.md` and `CITATION.cff` files inside each skill for the controlling notices and citation metadata.

## Scope

These tools support research navigation, mathematical development, and critical auditing. They do not turn analogy into theorem, numerical failure into impossibility, population obstruction into finite-sample detection, or citation into commercial permission. Exact claims should always be checked against their stated assumptions, proofs, evidence contracts, and historical sources.
