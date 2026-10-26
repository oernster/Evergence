# Evergence: Integration Up Levels and Martian Atmospheric Engineering

[← Evergence](../README.md) · [Mathematics](../MATHEMATICS.md) · [Economics](../ECONOMICS.md) · [Research](../RESEARCH.md)

**Status:** Proposed research extension, not an established physical theory or an approved engineering plan.  
**Parent framework:** [Evergence](https://github.com/oernster/Evergence)  
**Data infrastructure:** [TrellisDB](https://github.com/oernster/TrellisDB)  
**Initial engineering case:** Martian atmospheric and enclosed-habitat systems.

## 1. Purpose and scope

This document connects Evergence's concern for civilisational continuity and evolutionary possibility with an auditable mathematical modelling practice, provisionally named the **Integration Up Level (IUL) sequence**; it applies that practice to engineering feasibility on Mars.

Evergence provides the *reasons, values and prohibitions*. IUL provides a discipline for *building and validating mathematical models*. TrellisDB provides *small-scale experimental persistence*. Martian atmospheric engineering provides a *physically measurable test case*.

The investigation must continually distinguish:

1. **Values and normative commitments**, which require legitimate deliberation.
2. **Definitions and representations**, which may be convenient without being physically fundamental.
3. **Mathematical results**, which follow from stated assumptions.
4. **Scientific hypotheses and simulations**, which require empirical validation.
5. **Engineering proposals**, which must close mass, energy, throughput, stability, operations and safety budgets.

Mathematical elegance does not generate matter, energy or an atmosphere.

## 2. Incorporation by reference: the canonical Evergence material

This is an *extension*, not a replacement or duplication, of the existing work. The following documents in the Evergence repository remain authoritative for their respective subjects:

| Source | Role in the Mars work |
|---|---|
| [VISION.md](../VISION.md) | Continued life, agency, continuity, flourishing and revisable goals; habitation is a means, not an automatic end. |
| [ETHICS.md](../ETHICS.md) | No survival argument justifies coercion, atrocity or treating lives as optimisation variables. |
| [ARCHITECTS.md](../ARCHITECTS.md) | Competence, plural stewardship, accountability, appeals and replaceable authority. |
| [MEMORY.md](../MEMORY.md) | Preserve source data, discarded models, failed predictions, dissent and historical context, with responsible access controls. |
| [MATHEMATICS.md](../MATHEMATICS.md) | Balanced ternary, complex rotations, state spaces, coupled models, dimensional expansion, history-dependent transitions and limits of formalisation. |
| [COSMOLOGY.md](../COSMOLOGY.md) | Thermodynamic constraints and critical distinctions between supported physics and speculation. |
| [ECONOMICS.md](../ECONOMICS.md) | Scarcity, opportunity costs, energy budgets, incentives, intergenerational discounting and Goodhart failure modes. |
| [RESEARCH.md](../RESEARCH.md) | Explicit assumptions, counterexamples, falsifiability, versioned models and adversarial testing. |
| [GLOSSARY.md](../GLOSSARY.md) | Shared, carefully separated meanings of physical, mathematical and normative terminology. |
| [care-and-influence](../care-and-influence/README.md) | Caring action, autonomy and the responsibilities that accompany influence. |
| [civilisational-resilience](../civilisational-resilience/README.md) | Resilience, access to capability and avoidance of coercive biological selection. |
| [governance-integrity](../governance-integrity/README.md) | Reviewable authority, restraint, accountability and protection against institutional capture. |
| [linguistic-evolution](../linguistic-evolution/README.md) | Durable knowledge transfer while preserving the original context and meaning of scientific records. |

No single numerical utility or 'flourishing score' is assumed to subsume these commitments. Engineering feasibility is necessary for a deployable intervention but does not establish social or ethical permission.

## 3. What the mathematical concepts mean here

### 3.1 Dimensionality: three concepts must not be conflated

- **Physical state-space dimensions:** Variables required to describe a dynamical system, e.g. gas inventories, temperatures and available energy.
- **Representational dimensions:** Coordinates, phase states, balanced-ternary labels or experimental scenario descriptors. A balanced-ternary state space with D independent positions has 3^D labelled configurations but many may be physically impossible.
- **TrellisDB address dimensions:** Fixed-length tuples of strings used to store and retrieve JSON documents. These are not spatial, physical or algebraic dimensions by themselves.

An increase in any of these quantities is not by itself evidence of an extra physical dimension or greater wellbeing.

### 3.2 History-dependent transitions

Evergence proposes a schematic transition:

$$
C_{n+1}=F(C_n,H_n,\Delta D_n).
$$

For this application:
- $C_n$ is the modelled inhabited environment and the institutions responsible for it at stage n.
- $H_n$ is the accessible evidence and decision history, including rejected proposals.
- $\Delta D_n$ records additional modelled capabilities or degrees of freedom, not presumed extra spacetime dimensions.
- $F$ is initially a *research object*, not a known law of nature.

The physical component will instead use independently validated differential equations. The societal component requires transparent, participatory deliberation beyond the scope of a physical solver.

### 3.3 Balanced ternary as a possible representation

An experimental policy state might be encoded as $-1,0,+1$ for rejected, under review and provisionally supported. Such labels are administrative semantics, not intrinsic properties of matter or proofs of scientific validity. Competing binary and continuous representations should be benchmarked; no requirement to preserve ternary encoding if it performs worse.

## 4. IUL: rigorous definition and non-negotiable constant rule

Let $f(t)$ be any sufficiently integrable scalar or vector-valued rate, with reference time $t_0$. Define the sequence $I_n$ by

$$
I_0(t)=f(t), \qquad \frac{d I_n}{dt}=I_{n-1}(t)\quad(n\geq1).
$$

The general family of repeated antiderivatives is

$$
\boxed{I_n(t)=\frac{1}{(n-1)!}\int_{t_0}^{t}(t-s)^{n-1}f(s)\,ds
+\sum_{j=1}^{n} C_j\frac{(t-t_0)^{n-j}}{(n-j)!}.}
$$

Every integration creates a new independent constant $C_j$ (or vector for vector-valued rates). Earlier constants accumulate as polynomials. For partial integration, a 'constant' may be an arbitrary function of all variables not integrated over.

**Mandatory calculation protocol:**

1. Declare integrand, integration variable, coordinate frame and units.
2. State all fixed and varying quantities.
3. Write a single integration step, including its new constant or arbitrary function.
4. Preserve all previously introduced constants.
5. Verify by differentiation before moving to the next step.
6. Fix constants *only* using stated boundary or initial conditions, never by convenience.
7. Test dimensional consistency and applicable conservation laws.
8. Distinguish the mathematical antiderivative from any asserted physical interpretation.

An example: if $f(t)=\dot M_{O_2}(t)$ has units kg/s, then $I_1=M_{O_2}$ has units kg and its independent constant is the initial oxygen mass. $I_2$ has units kg·s and is **not** another source of oxygen.

The earlier relativistic test case $E=\gamma mc^2$ can remain a mathematical verification fixture, with integration over $\beta=v/c$; it does not replace electrochemical thermodynamics or atmospheric mass conservation.

## 5. First physical Mars model: a coupled inventory ledger

Define a provisional planetary or regional state vector:

$$
\mathbf{x}(t)=
\begin{bmatrix}
M_{CO_2}&M_{CO}&M_{O_2}&M_{N_2}&M_{H_2O}&U&T
\end{bmatrix}^{T}.
$$

The quantities comprise species inventories (kg), stored/internal energy (J) and representative temperature (K). Additional models may require altitude-dependent composition, soil/ice reservoirs, radiative transfer, power infrastructure and local pressure.

Represent atmospheric and industrial transformations as

$$
\boxed{\dot{\mathbf{x}}=S\,\mathbf{r}(\mathbf{x},\mathbf{u},t)
+\mathbf{b}_{\rm import}-\mathbf{b}_{\rm escape}-\mathbf{b}_{\rm sink}}
$$

for appropriately selected mass states, with a **separate, dimensionally appropriate energy equation** for the energy and thermal states. $S$ is a reaction stoichiometry or conversion matrix, $\mathbf r$ contains rates and $\mathbf u$ contains controlled inputs such as electricity, heaters and industrial duty cycles. Not every component shares the same physical units, so implementations must keep explicit units by variable and operator.

### 5.1 The minimum demonstrator: carbon dioxide electrolysis

MOXIE demonstrated:

$$
2CO_2\rightarrow2CO+O_2.
$$

With oxygen output rate $R_{O_2}$ in kg/s, ideal stoichiometry implies:

$$
\dot M_{CO_2}=-\frac{44}{16}R_{O_2},\quad
\dot M_{CO}=\frac{28}{16}R_{O_2},\quad
\dot M_{O_2}=R_{O_2}.
$$

**Mass closure test:** $-44/16+28/16+1=0$. The reaction does not create additional total mass. To accumulate useful oxygen, the coproduct CO, possible re-oxidation, atmospheric losses and energy inputs must be included.

For oxygen:

$$
\dot M_{O_2}=R_{O_2}-L_{O_2}-Q_{O_2}.
$$

**IUL level 1** integrates this net rate:

$$
M_{O_2}(t)=\int (R_{O_2}-L_{O_2}-Q_{O_2})\,dt+C_1.
$$

With specified initial state $M_{O_2}(t_0)=M_{O_2,0}$, the value of $C_1$ is fixed, equivalently:

$$
M_{O_2}(t)=M_{O_2,0}+\int_{t_0}^{t}(R_{O_2}-L_{O_2}-Q_{O_2})(s)\,ds.
$$

**IUL level 2** integrates the full level 1 expression:

$$
A_{O_2}(t)=\int M_{O_2}(t)\,dt+C_2.
$$

$A_{O_2}$ has units kg·s, an inventory-time exposure measure; $C_2$ is independent and is fixed only by a stated condition for $A_{O_2}$. No new mass is implied.

### 5.2 Partial derivatives and eigenanalysis

For a selected equilibrium or reference trajectory, linearise the physical dynamics with

$$
J_{ij}=\frac{\partial f_i}{\partial x_j}.
$$

Evaluate eigenpairs $J\mathbf q_i=\lambda_i\mathbf q_i$ to identify locally growing, decaying and oscillatory modes. Eigenvectors provide local relationships between perturbations; they are not substitutes for nonlinear simulations or evidence of a new physical interaction.

### 5.3 Validation gates

At each time step and each integrated level, verify:

- Species and element balances, including carbon and oxygen atoms.
- Energy conservation with accounted inputs, sinks and thermodynamic minimum work.
- Nonnegative physical inventories and temperatures in permissible ranges.
- Explicit units; numerical method convergence against time-step refinement.
- Initial conditions and every IUL integration constant.
- Calibration against published observations or independently reproducible benchmarks.
- Sensitivity to uncertain rates, resources and loss mechanisms.
- Preserved provenance, failed cases and competing interpretations.

## 6. Feasibility: global Mars and regional engineering are different targets

As of May 2026, an open-access analysis in *APS Open Science* reports that Mars requires roughly $3.89\times10^{15}$ kg of atmosphere per millibar of global mean surface pressure. A representative human-breathable open atmosphere with oxygen partial pressure of 21 kPa and nitrogen partial pressure of 50 kPa implies roughly $9.0\times10^{17}$ kg of oxygen and $1.9\times10^{18}$ kg of nitrogen, respectively. Its benchmark reversible work for oxygenation by water electrolysis is on the order of $1.3\times10^{25}$ J before real losses. It concludes that no surveyed abiotic global pathway closes *all* inventory, heating, production, power, retention and operations constraints. [Turyshev, 2026](https://doi.org/10.1103/krb8-h3v3).

These are order-of-magnitude feasibility limits, not the output of the proposed IUL implementation. Warming mechanisms, including [engineered aerosols modelled in 2024](https://doi.org/10.1126/sciadv.adn4650), do not themselves supply the needed bulk atmospheric gas.

Accordingly, distinguish:

- **Scenario A: Enclosed oxygen and life-support production**. Track oxygen and buffer gas inside a controlled volume, plant power and heat, leakage, storage, reliability and operational hazards.
- **Scenario B: Regionally covered or paraterraformed habitats**. Add coverage area, membrane loads, repair, thermal balance, biosystems and modular expansion.
- **Scenario C: Global atmospheric transformation**. Maintain as a long-horizon research scenario with explicit pass/fail conditions for gas inventory, sourcing, transport, power, temperature, sinks, atmospheric loss and future operations. Do not represent it as an available engineering design.

The program may produce valuable engineering discoveries even if Scenario C never becomes feasible.

## 7. Ethical, scientific and institutional gates from Evergence

**Before any intervention proceeds beyond simulation or reversible laboratory testing:**

- Assess planetary protection, including contamination risks and the possibility of extant Martian life; protect irreplaceable scientific evidence.
- Document environmental effects and alternative scenarios, including non-intervention and reversible habitation.
- Keep human autonomy, informed governance, other conscious life and future generations in scope.
- Separate technical recommendations from legitimate authority to approve an intervention.
- Provide independently auditable data and version histories; keep original records alongside later corrections.
- Avoid single-score optimisation that can conceal harms. Preserve explicit non-negotiable constraints, dissent, uncertainty and alternatives.
- Declare treatment of discount rates, finite resources and opportunity costs; do not make survival contingent on an unargued financial objective.

The ability to engineer something does not by itself imply that it ought to be done.

How settlements that later develop independently might be governed, with Earth-to-Mars heritage, scoped operational agreements and political claims kept as separate relations, is taken up in [plural rooting](../plural-rooting/README.md). Nothing there alters the physics here; no physics follows from a governance analogy.

## 8. TrellisDB role and sample experimental schema

TrellisDB's fixed-length tuple-of-string keys are suitable for a correctness-first prototype. Keep numerical solvers in a separate package. Example fixed five-dimensional key:

```
(scenario_id, run_id, region_id, simulation_time, record_type)
```

Example, consistent with the public library's API:

```python
from trellisdb import TrellisDB

with_db = TrellisDB.create("./mars_prototype.json", dimensions=5)
with_db.set(
    ("enclosed-oxygen", "run-0001", "habitat-a", "t-000000", "state"),
    {
        "model_version": "0.1-proposed",
        "time_s": 0,
        "inventories_kg": {"co2": 1000.0, "co": 0.0, "o2": 0.0},
        "initial_conditions": {"oxygen_mass_kg": 0.0},
        "units": {"mass": "kg", "time": "s"},
        "provenance": "illustrative synthetic starting state; not a measured Mars value",
    },
)
with_db.commit()
```

Every durable scientific result should additionally include: model version/commit, units, parameter assumptions, sources and source dates, integrator method, integration constants or boundary conditions, uncertainty bounds, conservation residuals, run ID and any validation status.

**Important limitation:** Atomic replacement makes a commit crash-resistant; it does **not** by itself provide immutable historical versions or unlimited-size high-frequency simulation storage. Implement append-only run identities, hashes and external backups at the application level. For large trajectories, store chunked numerical arrays in a suitable scientific file format and index their metadata and hashes in TrellisDB.

## 9. Development sequence and acceptance criteria

### M0: Canonical synthesis
- This document links, rather than overwrites, Evergence's existing values and mathematics.
- Record all epistemic categories and conceptual distinctions.
- Adopt a source/assumption ledger.

### M1: IUL mathematical verification
- Implement a general repeated-integral evaluator with explicit independent constants.
- Check derivatives numerically and analytically, when possible.
- Test vector-valued and partial-antiderivative cases.
- Treat the relativistic energy integration as an analytic regression fixture, not as oxygen chemistry.

### M2: MOXIE-class material balance model
- Implement CO2-to-CO-plus-O2 stoichiometry.
- Track all product masses, sources, sinks and electrical-energy accounting.
- Verify mass closure, nonnegative inventories and initial constants.
- Reproduce illustrative published oxygen-production benchmarks without pretending they establish continuous plant performance.

### M3: Coupled engineering demonstration
- Add enclosure pressure/temperature, power limits, losses and a controllable production plant.
- Produce time histories and local Jacobian/eigenmode diagnostics.
- Compare at least two realistic architectures using uncertainty intervals.

### M4: Scaling and feasibility boundaries
- Contrast local, covered-regional and global systems.
- Calculate gas, power, area, throughput, duration and maintenance constraints.
- Fail any global scenario which lacks a physically identified gas source or cannot close its budgets.

### M5: Independent scrutiny
- Invite criticism from atmospheric science, electrochemistry, industrial engineering, biosecurity and governance specialists.
- Archive rejected models, corrections and test failures.
- Distinguish demonstrated, modelled and speculative findings in every published result.

## 10. Immediate next experiment

**Question:** For a *specified enclosed habitat*, how does oxygen inventory evolve when a CO2 electrolysis plant operates at a limited production rate with electrical-power and leakage constraints?

Deliver: executable solver, conservation-test suite, stored TrellisDB scenario, simple time-series plots and a published table of assumptions and failure conditions. This produces a usable engineering artefact while leaving open the broader Mars ambition.

## References

1. [Evergence repository and core documents](https://github.com/oernster/Evergence).
2. [TrellisDB repository, README and architecture](https://github.com/oernster/TrellisDB).
3. [NASA (2023), MOXIE completes Mars mission](https://www.nasa.gov/solar-system/nasas-oxygen-generating-experiment-moxie-completes-mars-mission/).
4. [Jakosky and Edwards (2018), Inventory of CO2 available for terraforming Mars](https://doi.org/10.1038/s41550-018-0529-6).
5. [Ansari et al. (2024), Feasibility of keeping Mars warm with nanoparticles](https://doi.org/10.1126/sciadv.adn4650).
6. [McKay et al. (2025), The case for Mars terraforming research](https://doi.org/10.1038/s41550-025-02548-0).
7. [Turyshev (2026), Terraforming Mars: Mass, forcing and industrial throughput constraints](https://doi.org/10.1103/krb8-h3v3).
8. [NASA/JPL, Planetary Protection](https://planetaryprotection.jpl.nasa.gov/mission-implementation).

---

*This proposal belongs beside the current Evergence documents. It does not alter existing repositories, grant anyone authority over Mars or claim that planetary terraforming is presently feasible.*
