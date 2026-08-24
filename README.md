# Elimination Geometry Research Tools

> Cross-disciplinary research tools for applying **Elimination Geometry (EG)** across mathematics, statistics, artificial intelligence, information and computational sciences, optimization, control and decision sciences, quantum and physical sciences, engineering, economics, and life, health and Earth systems.

> **Equip your AI with EG—and turn it from an answer engine into a discovery engine.**

[Elimination Geometry — arXiv:2608.17646](https://arxiv.org/abs/2608.17646)

## What is Elimination Geometry?

Elimination Geometry studies the gap between solving a problem **locally** and realizing those local solutions through **one shared, deployable mechanism**.

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

## Featured success case: an EG-guided information-theory discovery

### Marton's inner bound is strictly sub-optimal

**Mian Huang, Yanxiao Liu, and Yi Liu**,  
*Sub-optimality of Marton's Inner Bound for the Two-Receiver Broadcast Channel*  
[[arXiv abstract](https://arxiv.org/abs/2608.19869)] [[PDF](https://arxiv.org/pdf/2608.19869)]

Marton's inner bound, introduced in 1979, has remained the best-known achievable region for the general two-receiver discrete memoryless broadcast channel. Whether it always equals the capacity region was a longstanding open problem. This work proves that it does not: there exist broadcast channels whose capacity region is strictly larger than Marton's inner bound.

The paper records a concrete use of Elimination Geometry in the discovery process. As one strand of the collaborative search, the first author used an **AI-guided, iterative, and structure-driven method based on EG**, allowing the failure of one structural conjecture to identify the next target. The resulting chain passed through counterexamples to the Markovity/rectangular-mapping conjecture, local tensorization and additivity, and then to fixed-input and unconstrained versions of Marton's optimality conjecture.

The final result does not rest on numerical search alone. The paper turns the discovered structure into a rigorous argument using finite auxiliary-variable reductions, a gradient-shaping construction, a constraint-removal theorem, exact rational data, and outward-rounded interval arithmetic.

> **Why this matters for EG.** This is a completed example of EG functioning within a collaborative discovery process as a research method rather than merely a vocabulary: elimination exposed a structural sequence of increasingly consequential failure modes, AI helped search the resulting restricted spaces, and conventional mathematical proof converted the discovered witness into a theorem resolving a major information-theory question.

## A cross-disciplinary research map

The same local-to-global structure appears under different names across science and engineering. The map below is deliberately broad, but it must be read with an important distinction:

- A **corpus anchor** means that the current monograph or 33-paper collection contains an explicit EG formulation, theorem, calibration, worked example, or research development in at least part of that area.
- A **research interface** means that the area contains promising elimination-and-deployment problems, but a genuine EG result still requires a domain-correct objective, an exact elimination identity, an admissible shared architecture, and new mathematics or evidence. Inclusion in this map is not a claim that such a result has already been proved.

### Mathematics and foundational methods

- **Convex and variational analysis — corpus anchor:** Legendre duality, Bregman defects, partial minimization, saddle elimination, convex–concave structure, proximal constructions, variational inequalities, strong convexity, and stability of argmin maps.
- **Geometry, topology, and singularity theory — corpus anchor:** fibers and quotients, bundles and atlases, monodromy, discriminants, degree, stratification, catastrophe taxes, integrability, Hodge repair, and topological obstructions to a continuous global choice.
- **Graph theory and network mathematics — corpus anchor:** graph-indexed distributions, graph smoothing, flow duality, cuts and cycles, holonomy, message transmission, network quotients, and graph-constrained deployment.
- **Combinatorics and discrete mathematics — research interface:** finite set systems, matroids, matchings, colorings, constraint-satisfaction problems, discrete Morse structures, combinatorial topology, and local witnesses that cannot be assembled into one global feasible object.
- **Discrete and combinatorial optimization — research interface:** mixed-integer optimization, polyhedral and conic lifts, integrality gaps, decomposition, scheduling, routing, facility location, branch-and-bound state, and resource-constrained approximation.
- **Functional, operator, and spectral analysis — corpus anchor:** eigenvectors and eigenspaces, spectral branches, operator-valued elimination, invariant subspaces, Schur complements, approximate spectral certificates, and matrix-free deflation.
- **Differential equations and dynamical systems — mixed:** ordinary, partial, stochastic, and differential-algebraic equations; closure, multiscale reduction, homogenization, singular perturbation, bifurcation, stability, inertial manifolds, and reduced-order dynamics. Mori–Zwanzig closure and multiscale dynamics are current corpus anchors; the wider PDE program is a research interface.
- **Numerical analysis and scientific computing — mixed:** surrogate and reduced-order models, iterative solvers, preconditioning, deflation, adaptive discretization, multigrid, domain decomposition, operator compression, error certification, and structure-preserving approximation. Exactification and certified deflation are current anchors.

### Statistics, machine learning, and artificial intelligence

- **Mathematical statistics — corpus anchor:** likelihood and profile elimination, latent-variable models, EM, estimating equations, proper scores, confidence sets, partial identification, model conflict, finite-sample certificates, and resolution complexity.
- **Bayesian and computational statistics — corpus anchor:** variational inference, posterior compression, amortized inference, nuisance elimination, approximate inner solutions, Monte Carlo surrogates, and the separation of posterior guidance from frequentist certification.
- **Time-series, spatial, and dependent-data statistics — corpus anchor:** dependence-aware defects, long-memory forecasting, state compression, change of scale, graph-indexed observations, and recursive sufficiency.
- **Causal inference and experimental design — research interface:** nuisance adjustment, mediator or latent-state elimination, transport across environments, task-specific identification, adaptive acquisition, sequential experiments, and certificates for interventions chosen under uncertainty.
- **Machine learning — corpus anchor:** representation learning, multitask learning, meta-learning, amortized prediction, graph learning, generative and latent-variable models, model compression, distillation, architecture comparison, and obstruction-aware learning.
- **Deep learning systems — mixed:** shared encoders, mixture-of-experts routing, neural operators, recurrent and memory architectures, attention bottlenecks, conditional computation, low-rank adaptation, and deployment under compute or communication limits. The architectural audit is anchored; model-family-specific theorems remain research interfaces.
- **Artificial intelligence and agent systems — research interface:** planning, search, tool use, world models, retrieval, long-horizon memory, multi-agent coordination, neuro-symbolic systems, reusable reasoning modules, and the distinction between current-task sufficiency and recursive closure.
- **Reinforcement learning and sequential learning — mixed:** policies, value functions, Bellman elimination, state abstraction, partial observability, offline-to-online transfer, exploration, regret, and adaptive structural expansion. Shared-policy and recursive-state questions are current anchors.
- **Scientific machine learning — research interface:** physics-informed learning, learned closure, operator learning, surrogate simulation, inverse problems, reduced-order discovery, and digital twins whose shared representations must preserve task-visible fine-scale structure.

### Information, computation, and security

- **Information theory — corpus anchor:** rate–distortion, information radius, task-relevant compression, certificate information bottlenecks, data processing, worldwise KL separation, communication–sample tradeoffs, and recursive rate–distortion.
- **Coding and communication theory — mixed:** source and channel coding, distributed coding, finite-blocklength reliability, feedback, semantic communication, network information flow, causal coding, and task-dependent decoders. Several information and certificate interfaces are anchored; full coding theorems are direction-specific.
- **Signal processing and imaging — mixed:** sampling, wavelets, compressed sensing, denoising, inverse imaging, sensor fusion, spectral estimation, adaptive acquisition, and task-visible compression. Certificate-directed wavelet acquisition is a corpus anchor.
- **Theoretical computer science — research interface:** algorithms and complexity, streaming and sketching, online algorithms, communication complexity, approximation algorithms, data structures, distributed computation, and resource lower bounds derived from lost oracle distinctions.
- **Programming languages and formal methods — mixed:** operational semantics, contextual equivalence, abstract interpretation, program refinement, compiler passes, proof-carrying transformations, model checking, and compositional verification. Context-safe replacement and operational observability are corpus anchors.
- **Databases and distributed systems — research interface:** query planning, view selection, data integration, consistency models, caching, replicated state, distributed summaries, and when a local query-optimal representation cannot be deployed as one shared schema or protocol.
- **Cryptography, privacy, and security — research interface:** cryptographic protocols, secure multiparty computation, zero knowledge, secret sharing, differential privacy, privacy-preserving learning, adversarial robustness, leakage channels, and cyber-physical security. EG would require a precise security/task defect and cannot infer cryptographic security from information loss alone.

### Decisions, control, games, and economic systems

- **Control theory — corpus anchor:** stochastic and robust control, entropy-regularized control, control as inference, state estimation, finite-memory control, model predictive control, system identification, and the transmission of local model defects into closed-loop loss.
- **Robotics and autonomous systems — research interface:** perception–control compression, localization and mapping, motion planning, manipulation, multi-robot coordination, embodied memory, safety filters, and deployable policies under sensing and compute limits.
- **Game theory and strategic learning — corpus anchor:** strategic regret, best-response or equilibrium objects, repeated and stochastic games, learning in games, information-limited play, recursive strategic state, and multi-agent coordination.
- **Economics and econometrics — mixed:** structural and dynamic models, latent heterogeneity, sufficient-state reduction, mechanism design, market design, industrial organization, matching, dynamic discrete choice, and policy deployment across heterogeneous agents. Strategic and statistical interfaces are anchored; domain-specific identification remains to be established.
- **Finance and market design — corpus anchor in part:** market microstructure, limit-order-book event order, execution-visible states, information compression, portfolio or risk-state aggregation, algorithmic execution, and sequential decision-making under operational constraints.
- **Operations research and service systems — corpus anchor in part:** queueing, state-space collapse, scheduling, inventory, supply chains, transportation, logistics, revenue management, and resource allocation. Task-visible queueing reductions are current anchors.

### Quantum and physical sciences

- **Quantum mechanics — corpus anchor:** density operators, quantum relative entropy, noncommutative state elimination, measurement-dependent visibility, spectral subspaces, and the difference between classical and quantum realizability.
- **Quantum information and quantum computing — mixed:** quantum channels, measurements, state compression, entanglement-sensitive representations, quantum control, variational quantum algorithms, tensor-network truncation, quantum error correction, and compilation under restricted gate or measurement architectures. Noncommutative rigidity is anchored; most algorithmic applications remain research interfaces.
- **Statistical physics and thermodynamics — corpus anchor:** free-energy defects, coarse-graining, renormalization, entropy production, nonequilibrium paths, diffusion, hidden dissipation, and task-conditioned macrostates.
- **Complex systems and interacting particles — research interface:** kinetic limits, collective behavior, spin systems, disordered systems, phase transitions, emergent macrostates, agent-based models, and task-relative coarse variables.
- **Classical and continuum mechanics — research interface:** elasticity, plasticity, fracture, contact, multibody systems, constitutive reduction, finite-element model reduction, and elimination of unresolved internal variables.
- **Fluid mechanics — research interface:** turbulence and closure, large-eddy simulation, multiphase and reacting flows, boundary layers, geophysical fluids, flow control, data assimilation, and reduced-order models that must retain task-visible coherent structures.
- **Wave physics, optics, and acoustics — research interface:** wave propagation, geometrical and wave optics, photonics, diffraction, inverse scattering, computational imaging, acoustics, aeroacoustics, vibration, seismology, and reduced representations constrained by phase, polarization, coherence, or boundary data.
- **Electromagnetism and plasma physics — research interface:** Maxwell solvers, antenna and inverse design, electromagnetic scattering, plasma closure, kinetic-to-fluid reduction, reduced-order field models, and multiscale coupling.
- **Chemistry and molecular science — research interface:** reaction networks, chemical kinetics, molecular dynamics, electronic-structure reduction, free-energy surfaces, coarse-grained molecular models, catalysis, and uncertainty-aware reaction-state compression.

### Engineering and designed materials

- **Composite materials and microstructure — research interface:** microstructure-to-property maps, representative volume elements, homogenization, multiscale constitutive laws, damage and failure, process–structure–property links, and whether one reduced material descriptor can serve all loading paths and tasks.
- **Metamaterials and architected media — research interface:** mechanical, acoustic, photonic, and electromagnetic metamaterials; topology optimization; band-structure design; multiscale resonances; and task-specific effective parameters.
- **Structural, civil, and geotechnical engineering — research interface:** structural health monitoring, reduced structural models, reliability, earthquake engineering, soil–structure interaction, porous media, and sensor-limited damage localization.
- **Mechanical, aerospace, and automotive engineering — research interface:** aerodynamic and structural design, propulsion, combustion, thermal management, guidance and navigation, fault diagnosis, digital twins, and certification under shared onboard resources.
- **Electrical and electronic engineering — mixed:** circuits, communication systems, estimation, control, power electronics, sensor networks, chip design, hardware-aware AI, and signal representations constrained by bandwidth, energy, latency, or precision.
- **Chemical and process engineering — research interface:** process control, reactor networks, separation, multiscale transport, reduced kinetics, process monitoring, fault diagnosis, and deployment across operating regimes.
- **Manufacturing and design engineering — research interface:** topology and multidisciplinary design optimization, additive manufacturing, process planning, quality control, surrogate-based design, and transferable digital twins.
- **Energy systems — research interface:** power grids, batteries, electrochemical systems, renewable integration, energy markets, demand response, storage control, and cross-scale models linking material state to system operation.

### Life, health, Earth, and environmental systems

- **Systems and computational biology — research interface:** gene regulation, signaling and metabolic networks, population dynamics, phylogenetics, molecular coarse-graining, cell-state representations, and multiscale biological models.
- **Neuroscience — research interface:** neural population codes, latent-state models, dynamical systems, connectomics, task-dependent neural compression, brain–computer interfaces, and representations that must remain sufficient under future updates.
- **Medicine and public health — research interface:** medical imaging, clinical prediction, personalized treatment, pharmacometrics, physiological digital twins, epidemiology, adaptive trials, and deployment across heterogeneous populations and institutions.
- **Earth, climate, and environmental science — research interface:** atmosphere–ocean models, climate parameterization, hydrology, subsurface flow, remote sensing, seismic inversion, weather prediction, ecosystem models, and cross-scale uncertainty propagation.
- **Infrastructure and networked systems — mixed:** transportation, communication networks, cloud and edge systems, smart cities, water networks, supply networks, resilience, cascading failures, and distributed decision-making. Queueing and operational-state examples are current anchors.

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

## What is included?

This repository contains two independent, self-contained research skills.

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

Both skills contain the complete Version 1.9 monograph source snapshot, the **Core16** manuscripts, and the **Extend17** domain extensions. They initialize a compact canonical research memory and reread exact chapters or papers on demand. They do not treat a summary, search hit, or analogy as a substitute for the underlying source.

## Research corpus

- **Core16** develops the common EG framework: certified elimination, native defects, the P/G/X/V/C design split, integrability and representation gates, composition, transfer, operational semantics, statistical certificates, architecture ledgers, adaptive learning, and exactification-based optimization.
- **Extend17** develops domain-facing research in information theory, strategic learning, time series and dynamical closure, statistical physics and renormalization, queueing, and market microstructure.

The distinction between *core* and *extension* describes logical role, not importance. Historical priority should be assessed at the level of the full problem contract and theorem chain: an inherited component formula must be credited, but a formula match alone does not establish identity of the surrounding framework.

## Example research questions

- What is the correct eliminated auxiliary object and native defect for a new scientific problem?
- Does a proposed architecture face a genuine realizability obstruction, or only an optimization failure?
- Which theorem assumptions are needed to transport a native defect into downstream task loss?
- Can finite data certify the obstruction, or must the answer remain unresolved?
- Which Core16 or Extend17 sources should be read for a particular domain?
- Is a proposed contribution mathematically new, a specialization, an integrated synthesis, or an analogy?

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
