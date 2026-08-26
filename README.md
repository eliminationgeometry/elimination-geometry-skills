# Elimination Geometry Research and Engineering Tools

**English** | [Chinese](README_CN.md)

> A cross-disciplinary Discovery Engine and engineering toolkit for applying **Elimination Geometry (EG)** across mathematics and optimization, information and computational sciences, artificial intelligence and statistics, control and decision sciences, engineering, quantum and physical sciences, economics, and life, health, and Earth systems.

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

This is not an arbitrary distance chosen after the fact. It measures excess cost directly in the original problem's own terms—for example prediction error, decision loss, energy difference, or another declared objective.

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

It also keeps four sources of failure separate: local-model approximation, architecture obstruction, finite-sample generalization, and implementation or optimization error. Moving from a mathematical obstruction to a scientific or engineering intervention also requires showing how the obstruction affects the final task, whether the existing system has exhausted its available capacity, and whether suitable independent evidence supports the conclusion.

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

- problem translation, five-part domain-fit screening, and formulation audits;
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

The two engineering skills are routed by the **dominant artifact and acceptance contract**: physical models, closures, and boundary conditions go to `eg-engineering-analysis`; implementation, concurrency, memory, and performance go to `eg-software-engineering`. Each independently includes the same on-demand cross-boundary protocol, remains self-contained, and does not invoke the other; mixed domains are mapped below.

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

Compression can likewise merge distinctions needed for deployment, certification, or future updates. EG's **no-compensation principle** does not say that resources can never be exchanged. It says that, without an explicit exchange theorem, quantities from different ledgers may not be added, substituted, or used to cancel one another. More data do not automatically remove an architecture obstruction; a larger deployment model cannot recover crucial information already discarded by the evidence interface; and better optimization cannot create distinctions absent from the representation. Typed accounting therefore prevents category errors, false causal diagnoses, and irrelevant interventions.

### 2. A heuristic engine: turn open problems into structured search

EG supplies reusable research heuristics. It first finds the smallest problem in which solving cases separately conflicts with requiring one shared solution, and compares “a solution for each case” with “one solution for every case.” It then looks for the smallest pair treated as identical by a shared representation even though they produce different task outcomes; the defect is always derived from the original objective rather than chosen as an arbitrary distance. Next it checks whether these internal differences actually affect the final task and searches edge cases, structural breaks, dependencies, and effects that appear only after repetition or composition for counterexamples. Each failed conjecture is used to generate a sharper, testable successor.

These heuristics do not guarantee novelty or replace proof. They narrow the search space, rule out interventions unrelated to the diagnosed obstruction, and organize exploration into a cycle of structural conjecture, minimal witness, transmission test, certificate, and repair. The counterexample cascade in the Marton case below is one representative instance of this discovery mechanism.

### 3. Certification and action: know when to conclude and what to do next

EG does more than analyze structural obstructions. It connects finite-data decisions, system-capacity limits, and the choice of the next intervention into a certification–action system. A confidence world retains every complete world compatible with the available data. The system reports “certified feasible” or “certified impossible” only when those worlds agree; otherwise it honestly reports “unresolved.” Even if every compatible world admits some feasible architecture of its own, there may still be no single architecture that is safe to deploy across all of them now.

EG also distinguishes three carriers that are not interchangeable by default. A deployment carrier preserves the oracle distinctions needed to act; an evidence carrier preserves the statistical distinctions needed to authorize a conclusion; and a recursive carrier preserves the state distinctions needed to choose future observations and continue updating. A failure witness therefore routes to a matching action: change the scientific model for local-model failure; change the sensor, statistic, or experiment for evidence blindness; split state or add memory for a recursive collision; change the representation, routing, or decoding method for a deployment collision; and spend more optimization or compute only when an admitted solution has merely not been reached.

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

The first three mechanisms explain why EG works as a research method. The fourth explains why AI can reuse and amplify that method reliably.

### 4. An executable research graph: make dispersed knowledge work together

A foundation model may already have encountered many of the methods and results needed for such problems: how to eliminate auxiliary variables, measure the cost of approximation or compression, recognize structural limits that prevent locally adequate solutions from being deployed together, and preserve uncertainty when the evidence is incomplete. Yet this knowledge is scattered across different literatures, disciplines, and contexts. After pretraining compresses a vast corpus into model parameters, the individual facts may remain while their cross-disciplinary links fail to be retrieved, ordered, and activated together for a new problem. The knowledge has not literally been deleted; the relevant relations may simply be weak links without a stable path of use.

EG organizes these dispersed ideas into a typed, evidence-bearing, action-linked **executable research graph**. It records not only which concepts exist, but which object came from which elimination, which defect uses which native unit, which carrier must preserve which distinction, which gate permits which inference, and which failure witness should trigger which action. A method for eliminating hidden factors and a tool for measuring the cost of deviation, for example, no longer remain concepts isolated in different literatures; their roles in the same problem place them within one complete reasoning chain.

The repository's four EG skills deploy this organization for different tasks: `eg-library` handles primary-source retrieval, verification, and synthesis; `eg-research-collaborator` develops unfamiliar problems into falsifiable research programs; `eg-engineering-analysis` serves physical, scientific, and multidisciplinary engineered systems; and `eg-software-engineering` serves code, software architecture, and runtime systems. Each uses a compact canon to preserve core relations and reasoning order, keeps the complete monograph and papers as traceable external memory, and rereads exact sources on demand for the problem at hand.

What EG gives an AI first is not more facts, but types, adjacency, retrieval order, evidence thresholds, and next actions among the facts it already has. It helps dispersed knowledge work together on the right problem and in the right order.

## Representative cases

### (1) Marton's inner bound is strictly suboptimal

**Mian Huang, Yanxiao Liu, and Yi Liu**,  
*Sub-optimality of Marton's Inner Bound for the Two-Receiver Broadcast Channel*  
[[arXiv abstract](https://arxiv.org/abs/2608.19869)] [[PDF](https://arxiv.org/pdf/2608.19869)]

Introduced in 1979, Marton's inner bound remained the best-known achievable region for the general two-receiver discrete memoryless broadcast channel. This work proves that it does not always reach the capacity region, resolving a longstanding optimality question.

The paper records EG's concrete role in the collaborative discovery process: AI-assisted structural search began with a counterexample to a narrower conjecture about channel structure, advanced through a sequence of stronger falsifiable statements, and eventually reached the key counterexample to Marton optimality; rigorous mathematics then completed the proof. It is a successful example of EG moving from structural diagnosis to an important theoretical discovery.

### (2) The Data Selection problem

**Mian Huang**  
*Exact Data Selection: Low Dimensions and Budget Two*  
[[Paper and DOI](https://doi.org/10.5281/zenodo.21712106)] [[COLT 2025 open problem](https://proceedings.mlr.press/v291/hanneke25e.html)]

When a learning algorithm is fixed and may retain only a small subset of a full dataset, which samples best preserve full-data performance? This work measures the performance loss directly by the additional squared error between the selected-sample mean and the full-data mean. It solves the low-dimensional case exactly and identifies how the transition at budget two changes with dimension. EG's role is to treat the selected samples as a budget-limited representation and price data compression in the original task loss, producing a clear “how much data versus how much performance” frontier.

### (3) Data analysis in quantum computing: “Correct on average” does not mean “reliable”

In quantum computing, researchers cannot read the full system state as they would ordinary data; they must combine many randomized measurements to estimate global properties. A method can be correct on average over the long run without being stable with finite data. Different aggregation rules can therefore have the same long-run average but very different fluctuations. **Correct local components do not guarantee a correct shared aggregation mechanism.**

EG audits the **estimation object**, **aggregation architecture**, and **final risk** separately: expose the aggregation bottleneck in a minimal case, prove its actual cost, and then apply a matched repair such as using a more complete set of sample combinations. The same obstruction–witness–repair route applies to batches, subgraphs, expert outputs, and distributed computation, while preventing local correctness from being overstated as a broad global guarantee.

## A cross-disciplinary research and application map

This map is intentionally selective. A subfield is included only when at least one standard problem can name all five parts of an EG contract: **(1)** a fine object and a genuine elimination, reduction, or local oracle; **(2)** one shared representation, model, mechanism, controller, protocol, or resource limit; **(3)** a native scientific or operational objective; **(4)** a minimal collision or witness showing that a discarded distinction can change that objective; and **(5)** field-specific validity checks and evidence. The mere presence of latent variables, compression, coarse-graining, or a low-dimensional model is not enough.

- A **direct EG anchor** means that the monograph or 33-paper collection already contains an explicit EG formulation, theorem, calibration, or worked example for part of the subfield.
- A **partly anchored transfer** combines a direct EG interface with domain work that has not yet been developed as a complete EG result.
- A **supported transfer direction** passes the five-part fit test in the field's primary literature, but remains a research proposal rather than an established EG theorem.

The labels apply only to the mechanisms named below, not to every problem in the surrounding discipline.

### Mathematics and foundational methods

- **Convex and variational analysis — direct EG anchor:** inner variables, dual variables, or lifts are eliminated into value functions or frozen surrogates; the native currencies are objective gap, stationarity, and curvature. Partial minimization, Bregman defects, saddle elimination, and exactification supply exact anchors.
- **Geometry, topology, and singularity theory — direct EG anchor:** local branches, charts, or fibers must be assembled into one global section, atlas, or continuation rule. Holonomy, degree, discriminants, and singular strata provide explicit witnesses to failed global choice.
- **Graph theory and network mathematics — direct EG anchor:** local states or messages are coupled through one graph-constrained representation. Cuts, cycles, flows, graph quotients, and holonomy expose distinctions that local checks miss.
- **Combinatorial structures and discrete optimization — partly anchored transfer:** fine feasible objects are replaced by a common relaxation, lift, decomposition, or bounded message space and judged by feasibility, integrality, or objective loss. Matching, assignment, finite graph flow, and extension complexity are direct anchors; routing, scheduling, and constraint systems require new domain-specific results.
- **Functional, operator, and spectral analysis — direct EG anchor:** auxiliary blocks or fine modes are replaced by a shared subspace, operator approximation, or preconditioner and judged by spectral or convergence error. Schur complements, invariant subspaces, Ritz certificates, and matrix-free deflation are explicit anchors.
- **Reduced dynamics, closure, and multiscale equations — partly anchored transfer:** unresolved degrees of freedom are replaced by one closure, memory state, or reduced model and judged by trajectories, fluxes, stability, or another declared quantity of interest. Mori–Zwanzig closure is a direct anchor; broader PDE, homogenization, and reduced-order questions require their own validity analysis.
- **Numerical analysis and scientific computing — partly anchored transfer:** a fine model or solve is replaced by a surrogate, sketch, low-rank model, discretization, or iterative solver and judged by task error, gradient error, convergence, and total computational cost. Exactification and certified deflation are direct anchors.

### Statistics, machine learning, and artificial intelligence

- **Mathematical statistics — direct EG anchor:** nuisance parameters, latent variables, or unresolved model choices are eliminated while one estimator, score, confidence procedure, or decision rule must serve the stated world. Profile likelihood, EM, proper scores, partial identification, confidence worlds, and finite-sample certificates are explicit anchors.
- **Bayesian and computational statistics — direct EG anchor:** posterior or latent structure is compressed into one variational family, amortized map, Monte Carlo surrogate, or approximate inner solution and judged by a declared inferential task. EG keeps posterior guidance, optimization error, and frequentist certification in separate ledgers.
- **Time-series, spatial, and dependent-data statistics — direct EG anchor:** history, scale, or graph-indexed dependence is compressed into a shared state or predictor and judged by forecast, evidence, or update loss. Long memory, dependence-aware defects, time-scale elimination, and recursive sufficiency are explicit anchors.
- **Causal representations and adaptive experiments — supported transfer direction:** low-level observations and nuisance mechanisms are compressed into one representation or acquisition policy across environments and judged by intervention identification or decision loss. Intervention environments and observationally equivalent states with different interventional consequences provide natural witnesses.
- **Machine learning and deep learning systems — partly anchored transfer:** examples, tasks, experts, or latent factors are compressed into a shared encoder, architecture, model, router, or low-rank adaptation under one resource budget. Representation collisions, multitask incompatibility, amortization gaps, and architecture obstructions are direct EG interfaces; model-family guarantees remain domain-specific.
- **Sequential learning, planning, and agent systems — partly anchored transfer:** histories and hidden state are compressed into a reusable state, memory, policy, world model, or tool interface and judged by future value, regret, safety, or recursive update accuracy. Shared-policy and recursive-state results are anchors; a one-step-useful memory is not automatically sufficient for future interaction.
- **Scientific machine learning and operator surrogates — supported transfer direction:** fine fields or simulators are replaced by one learned closure, neural operator, inverse map, or surrogate across regimes and judged by physical quantities of interest rather than training residual alone.

### Information and computation

- **Information theory — direct EG anchor:** a world, source, or evidence object is compressed into a shared carrier and judged by task distortion, certificate loss, or recursive update cost. Deployment information radius, certificate bottlenecks, data processing, and recursive rate–distortion are explicit anchors.
- **Coding and communication theory — partly anchored transfer:** sources or distributed observations are mapped through one finite-rate encoder, channel, or causal message protocol and judged by reconstruction, decision, or reliability loss. EG supplies task-relative and certificate interfaces; full source, channel, network, and finite-blocklength theorems remain coding problems.
- **Signal processing, sensing, and imaging — partly anchored transfer:** fine signals, phases, or scenes are replaced by samples, coefficients, measurements, or reconstructions under a common sensing budget and judged by a declared detection, estimation, or imaging task. Certificate-directed wavelet acquisition is a direct anchor.
- **Streaming, sketching, and communication-limited algorithms — supported transfer direction:** an input stream or distributed input is replaced by one bounded-memory sketch or message transcript and judged by its supported query or optimization workload. Collision witnesses and communication lower bounds make the lost distinctions operationally testable.
- **Programming languages and formal methods — partly anchored transfer:** concrete states or components are replaced through an abstraction, compiler pass, refinement, or pipeline substitution and judged by contextual behavior. Operational semantics and context-safe replacement are direct anchors; EG does not by itself prove memory safety, linearizability, or protocol correctness.
- **Database views, caches, and distributed state representations — supported transfer direction:** base data or event histories are replaced by shared views, cache keys, schemas, replicas, or summaries and judged by an explicit query workload or state-machine behavior. Workload-dependent view selection, stale-state collisions, and event-order witnesses meet the fit test.
- **Privacy-constrained representations — supported transfer direction, not a security theorem:** raw records are replaced by one randomized release, statistic, or learned representation and judged by task utility under a separately defined privacy constraint. EG can study the architecture–utility ledger; differential privacy, information-flow security, and adversarial guarantees must still be proved in their native formal systems. Core cryptographic security is not claimed here.

### Decisions, control, games, and economic systems

- **Control and estimation — direct EG anchor:** hidden state, disturbances, or model detail are replaced by one estimator, controller, belief state, or finite-memory policy and judged by closed-loop loss, stability, constraints, or safety. Defect transmission into control loss is an explicit anchor.
- **Game theory and strategic learning — direct EG anchor:** private histories or strategic states are compressed into one message, quotient, or shared strategy class and judged by regret, value, equilibrium error, or exploitability. Information-limited play and recursive strategic state are explicit anchors.
- **Structural and dynamic economics, econometrics, and mechanism design — partly anchored transfer:** heterogeneity or high-dimensional state is reduced to sufficient statistics, message spaces, or deployable policies and judged by identified economic targets, welfare, incentives, or counterfactual loss. EG interfaces are real, but identification and equilibrium claims remain model-specific.
- **Market microstructure and algorithmic finance — partly anchored transfer:** order-book history is compressed into event types or execution states and judged by prediction, execution, or regret. Event-order and execution-visible-state papers are direct anchors; portfolio and risk aggregation require separate contracts.
- **Operations research and service systems — partly anchored transfer:** detailed network or queue state is replaced by a collapse, schedule state, inventory summary, or shared allocation rule and judged by delay, deadlines, service, cost, or feasibility. Task-visible queueing collapse is a direct anchor; logistics and supply-chain extensions remain domain-specific.

### Quantum and physical sciences

- **Quantum mechanics — direct EG anchor:** quantum states or auxiliaries are reduced through channels, measurements, partial traces, or variational elimination and judged by a native quantum divergence or observable task. Noncommutative state elimination and measurement-limited visibility are explicit anchors.
- **Quantum information and quantum computing — partly anchored transfer:** states, channels, entanglement structure, or circuit descriptions are compressed into one measurement, tensor-network, gate, or error-correction architecture and judged by fidelity, observable error, or algorithmic performance. Noncommutative rigidity is anchored; algorithm- and hardware-specific claims are not yet EG results.
- **Statistical physics and thermodynamics — direct EG anchor:** microscopic states or paths are coarse-grained into shared macrostates or effective dynamics and judged by free energy, path loss, entropy production, or task-conditioned observables. Renormalization, diffusion, and hidden dissipation are explicit anchors.
- **Interacting-particle and kinetic coarse-graining — supported transfer direction:** particle configurations or distribution functions are reduced to moments, fields, or kinetic closures and judged by transport, collective behavior, phase, or stability. The direction is limited to problems with a declared closure and task; generic “complex systems” are not claimed.
- **Solid and continuum mechanics — supported transfer direction:** fine stress, contact, crack, or internal-variable fields are replaced by one constitutive law, reduced basis, or finite-element model and judged by force, deformation, failure, or stability across loading paths.
- **Fluid mechanics, transport, and plasma reduction — supported transfer direction:** unresolved scales, interfaces, kinetic variables, or memory are replaced by one closure, grid-scale model, or reduced basis and judged by flux, force, mixing, stability, control, or rare-event behavior. Equal coarse moments with different fluxes are natural witnesses.
- **Wave physics, optics, acoustics, and electromagnetics — supported transfer direction:** phase, polarization, coherence, evanescent content, fine geometry, or boundary traces are replaced by one measurement or effective-medium model and judged by focusing, scattering, imaging, band, load, or energy-transfer tasks.
- **Molecular coarse-graining and reaction-network reduction — supported transfer direction:** atomistic coordinates, intermediates, or reaction states are replaced by shared beads, potentials, lumped species, or reduced kinetics and judged by structure, thermodynamics, rates, transport, or dose response. Representability and transferability failures supply direct witnesses.

### Engineering and designed systems

- **Composite materials and microstructure — supported transfer direction:** constituent fields, interfaces, orientation, defects, and history are replaced by one RVE, homogenized tensor, descriptor, or constitutive family and judged by stiffness, transport, damage, fatigue, or failure. Microstructures with the same low-order descriptors but different properties are explicit witnesses.
- **Metamaterials and architected media — supported transfer direction:** fine resonant geometry is replaced by effective parameters or a shared unit-cell/design grammar and judged by band structure, transmission, focusing, stiffness, or another declared response. Spatial dispersion and nonlocal response test whether the effective representation is sufficient.
- **Structural, civil, and geotechnical systems — supported transfer direction:** fine modes, damage, cracks, contact, or soil heterogeneity are replaced by one reduced model, sensor layout, or health state and judged by reliability, localization, load capacity, or hazard response.
- **Mechanical, aerospace, and automotive systems — supported transfer direction:** multiphysics fields and high-fidelity simulations are replaced by shared onboard models, surrogates, controllers, or resource budgets and judged by mission, thermal, structural, propulsion, guidance, or fault-management performance.
- **Power, sensing, and hardware-constrained systems — partly anchored transfer:** network or signal detail is replaced by reduced grid models, sensor summaries, circuit abstractions, quantized representations, or hardware-limited inference and judged by stability, estimation, energy, latency, or precision. Information, control, graph, and resource ledgers provide anchors.
- **Chemical, process, and manufacturing engineering — supported transfer direction:** reaction intermediates, process fields, and expensive simulations are replaced by reduced kinetics, lumped plants, surrogate chains, or shared process descriptors and judged by yield, quality, control, safety, or process–structure–property performance across operating regimes.
- **Energy conversion, storage, and grids — supported transfer direction:** electrochemical microstate, degradation history, network contingencies, or fast variables are replaced by battery states, reduced plants, dispatch summaries, or controllers and judged by safety, lifetime, efficiency, resilience, or system cost.

### Mixed computational and cyber-physical engineering

- **Simulation software and computational engineering — partly anchored transfer:** governing-model state and numerical detail are reduced into executable discretizations, solvers, precision choices, and parallel representations and judged jointly by physical quantity-of-interest error, convergence, wall-clock cost, and reproducibility. Exactification and certified deflation are anchors; end-to-end model–code accounting remains to be developed.
- **Robotics and autonomous systems — partly anchored transfer:** physical and perceptual history is reduced into one embodied state, map, planner abstraction, estimator, or policy under sensing and compute limits and judged by closed-loop task success, safety, and recovery. Control and recursive-state interfaces are anchored; complete robotic certification is not.
- **Digital twins and model-based operations — supported transfer direction:** evolving physical state is reduced into one synchronized model, schema, estimator, and fidelity policy and judged by monitoring, prediction, intervention, or maintenance decisions. Staleness, model mismatch, versioning, and synchronization create concrete collision witnesses.
- **Cyber-physical, embedded, and real-time systems — partly anchored transfer:** plant, software, network, and clock state are reduced into shared interfaces, schedules, protocols, and runtime state and judged by end-to-end control, timing, robustness, and safety. Formal timing, concurrency, security, and certification obligations remain external authorities.

For these mixed fields, the two engineering skills share a lightweight cross-boundary contract: declare one goal spanning model and software, record the physical meaning, units, timing, and state at the interface, keep error sources and version provenance separate, and state both the information actually available to the system and the validation path from simulation to an independent endpoint. Passing this contract does not authorize code changes, hardware execution, deployment, experiments, or safety certification.

### Life, health, Earth, and environmental systems

- **Systems and computational biology — supported transfer direction:** biochemical species, pathways, or cell states are reduced into one lumped network, coarse state, or input–output model and judged by flux, dose response, phenotype, or intervention behavior. Reaction-network reductions that preserve one output but not another provide direct witnesses.
- **Computational neuroscience — supported transfer direction:** neural population activity and history are reduced into latent states, codes, or shared task representations and judged by decoding, behavior, control, or future update. Task-dependent remapping makes representation sufficiency empirically testable.
- **Clinical, physiological, and epidemiological model deployment — supported transfer direction:** patient, physiological, or contact-network detail is reduced into risk scores, latent states, compartments, or shared policies and judged by calibrated clinical or public-health decisions across populations and institutions. Cross-site shift and subgroup collisions are valid witnesses; EG is not a medical-validity or regulatory claim.
- **Earth, climate, and environmental modeling — supported transfer direction:** clouds, turbulence, topography, porous heterogeneity, ecosystem state, or forcing history is reduced into parameterizations, coarse grids, assimilation states, or sensor networks and judged by fluxes, extremes, hazards, forecasts, or interventions. Scale, conservation, and out-of-region validation are mandatory.

EG does not replace the established theories in any retained field. Its role is narrower: type the elimination, shared deployment restriction, native loss, transmission path, evidence, and repair. Broad fields for which that contract cannot yet be stated are deliberately left off the map.

### When does a new application genuinely become EG?

A defensible new application must identify:

1. the fine object, eliminand, and admissible local oracle;
2. an exact elimination/insertion identity or an explicit statement that the use is only analogical;
3. the shared architecture, resource, representation, or deployment contract;
4. the native objective and the pointwise/common, average/worst-case, fixed/adaptive quantifiers;
5. a zero-tax case and a positive collision or witness;
6. the transmission path from native defect to the declared task;
7. field-specific admissibility, finite-information evidence, saturation testing, and a mechanism-matched repair.

## Research corpus

All four skills contain the complete Version 1.9 monograph source snapshot, the **Core16** manuscripts, and the **Extend17** domain extensions. Each is independent and does not call another EG skill. They initialize a compact role-specific memory and reread exact chapters or papers on demand. They do not treat a summary, search hit, analogy, numerical failure, or engineering proxy as a substitute for the underlying source or evidence.

- **Core16** develops the common EG framework: starting from local elimination and its native cost, it asks whether one shared representation can serve different cases, separates the sources of failure, traces how a defect affects the task, and studies finite-data certification together with repairs in learning and optimization.
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
