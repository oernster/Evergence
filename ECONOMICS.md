# Economics, Resources and Incentives

[← README](README.md) · [Cosmology](COSMOLOGY.md) · [Research →](RESEARCH.md)

## Why economics enters

Survival over long horizons is allocation under constraint: of free energy, matter, time, institutional capacity and the capacity to remember. Economics is the discipline that studies allocation under scarcity, so its established results bear on the framework whether or not the framework borrows its vocabulary. It enters here as a **constraint set, not an objective** ([VISION.md](VISION.md): means are not ends). No result below is a reason to accumulate, grow or optimise; each is a reason a proposed survival mechanism may fail or distort.

## What is established and what is contested

Labels follow the conventions in [RESEARCH.md](RESEARCH.md).

- **Definition.** Scarcity: at any stage the free energy, matter and time available to a civilisation are finite, so a use of them forecloses other uses (opportunity cost). This holds for any physically embodied civilisation, whatever its institutions.
- **Mathematical result.** Present-value arithmetic: under exponential discounting at rate $r$, a benefit $B$ at time $t$ is valued at $Be^{-rt}$, so for any positive $r$ the far future is worth arbitrarily little. The arithmetic is not in doubt.
- **Normative.** The choice of $r$ when the benefit is the continued existence of a civilisation. Ramsey (1928) held that discounting the welfare of later generations is ethically indefensible; the dispute between the Stern Review (2006) and its critics (Nordhaus, 2007) over the climate discount rate is a dispute about values wearing the clothes of a parameter. This framework treats the rate of time preference across civilisational stages as a normative decision to be argued in [ETHICS.md](ETHICS.md), never as a market datum.
- **Empirical evidence.** People and institutions discount the near future more steeply than the far future (hyperbolic rather than exponential), which produces preference reversals. The behavioural evidence is well replicated; the modelling of it is contested.
- **Evidence-supported, contested in degree.** The economic process is entropic (Georgescu-Roegen, 1971): production turns low-entropy inputs into high-entropy waste and cannot be decoupled indefinitely from free-energy gradients. The thermodynamic premise is physics ([COSMOLOGY.md](COSMOLOGY.md)); how tightly it binds economic activity in practice (and over what horizon) is contested between ecological economists (Daly's steady-state proposal, 1977) and growth theorists (Solow, 1956; Romer, 1990). The framework takes no side on growth. It records that a growth imperative is not a survival requirement and may conflict with one.
- **Mathematical result, with an empirical record.** Non-excludable, non-rival goods are under-provided by uncoordinated self-interested agents (Samuelson, 1954). A habitable environment, a preserved record and the continued existence of a lineage are such goods; their beneficiaries include agents who do not yet exist and cannot pay. The empirical record points the useful way: Ostrom (1990) documented commons sustained over centuries by polycentric local institutions without privatisation or central control, which is evidence that under-provision describes a failure mode rather than a destiny.
- **Empirical evidence, with its degenerate case named.** Reward structures steer aggregate behaviour whatever the stated intention (Kerr, 1975); a measure that becomes a target ceases to measure (Goodhart, 1975). Mechanism design (Hurwicz, Maskin, Myerson) is the constructive discipline that asks which rules make the desired behaviour individually rational.
- **Mathematical result (physics).** Information has a thermodynamic cost: erasing one bit dissipates at least $k_BT\ln 2$ (Landauer, 1961); holding information against noise costs work continuously. An archive is not free to keep ([MEMORY.md](MEMORY.md)).

## Consequences for the framework

1. **Discounting is where a survival framework can die quietly.** (Hypothesis.) Any evaluation that applies a positive constant rate to civilisational continuity progressively reduces the present value it assigns to later stages. $Be^{-rt}$ stays positive at every finite $t$ and tends to zero only as $t\to\infty$, so no stage is valued at exactly nothing; over sufficiently long horizons, though, later stages can become practically negligible within the evaluation while their intrinsic moral significance is unchanged. The framework's ambition then carries almost no weight in the evaluation meant to serve it. The rate across stages is therefore declared in the open as a normative commitment and argued as one.
2. **Continuity is an intergenerational public good.** (Hypothesis.) Standard theory predicts its under-provision; the empirical record says institutions can overcome that. Which institutions is Workstream 2's question; Ostrom's design principles (clear boundaries, rules made by those they bind, monitoring by the governed, graduated sanctions, cheap conflict resolution, nested tiers) are the first candidates for [ARCHITECTS.md](ARCHITECTS.md) to test.
3. **Every target the framework sets is a Goodhart target.** (Hypothesis.) A population count, a resource share, a viability score, a configuration count: any of these made into an objective will be gamed by the structure around it. This is the economic form of the rejection of numerical balance in [ETHICS.md](ETHICS.md); the repair is to keep measures diagnostic and never make a measure the thing optimised.
4. **Incentives bend decisions whatever the charter says.** (Hypothesis, drawn from the author's Decision Architecture series, which treats incentive gradients as curvature in the space decisions move through; the geometric language is a figure of speech, not a computable metric.) An architect institution whose charter points one way and whose incentives point another will follow the incentives. Workstream 2 should therefore read incentives, not only mandates.
5. **A memory has a budget.** (Hypothesis.) Preservation competes for free energy with survival and with evolution; a complete archive kept forever is a physical impossibility on a finite budget, so the three duties in [MEMORY.md](MEMORY.md) are allocation decisions and should be costed as such.

## A toy budget

At stage $n$ let $W_n$ be the work available over the stage. The civilisation allocates it among survival $S_n$, memory $M_n$ and evolution $E_n$ (new degrees of freedom, [MATHEMATICS.md](MATHEMATICS.md) section 6):

$$
S_n+M_n+E_n\le W_n .
$$

Each term has a floor below which the corresponding aim fails: $S_n\ge S_n^{\min}$ for persistence; $M_n\ge M_n^{\min}$ for a faithful embedding $H_n\hookrightarrow H_{n+1}$; $E_n\ge 0$, with $\Delta D_n=0$ whenever $E_n=0$. Across stages $W_{n+1}$ depends on $E_n$ (new capability can open new resources) and on the cosmological supply ([COSMOLOGY.md](COSMOLOGY.md)); the rate of time preference decides how much of $W_n$ a stage is willing to spend on $W_{n+1}$.

This is a toy, labelled speculation. It carries no prices, no agents and no mechanism. Its use is to make the trade-off among the three aims explicit enough to argue about and to show that a civilisation choosing $E_n=0$ forever has chosen stagnation by budget rather than by decree.

## What economics does not settle

- Whose preferences count. A market prices what present agents will pay; the agents with the largest stake in continuity are not yet present; other conscious entities may not trade at all ([ETHICS.md](ETHICS.md)).
- What flourishing is. Welfare economics needs a welfare function; the framework holds that no single one should be imposed.
- Whether growth is required. Growth theory describes conditions under which output rises; it does not show that survival needs it; [VISION.md](VISION.md) rejects accumulation as an objective.

## Red-team questions for this document

- Is economic vocabulary smuggling a growth imperative back into a framework that rejects one?
- Has a discount rate been assumed anywhere without being argued?
- Is a market being assumed where there are no agents able to trade?
- Does the toy budget treat memory as a cost to be minimised rather than a duty with a floor?

## Next

See [RESEARCH.md](RESEARCH.md) for the investigation plan, including Workstream 6.
