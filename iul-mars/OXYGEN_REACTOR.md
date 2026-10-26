# Mars: producing breathing oxygen with an electrochemical reactor

[← IUL and Mars](README.md) · [Evergence](../README.md) · [Ethics](../ETHICS.md) · [Research](../RESEARCH.md)

> **Status:** Proposed engineering research extension for Evergence v0.8.0. The chemistry has been demonstrated on Mars by NASA's MOXIE experiment. A permanent, crew-rated plant or a facility inside Olympus Mons has **not** been demonstrated or approved. This document does not claim to make the open Martian atmosphere breathable.

## Public-facing summary

Mars already contains abundant oxygen atoms; most are chemically bound in carbon dioxide (CO₂) rather than present as breathable molecular oxygen (O₂). Evergence proposes investigating an industrial reactor that draws in the thin Martian atmosphere, filters and compresses its carbon dioxide, heats it and uses electrical energy to separate that carbon dioxide into oxygen and carbon monoxide. The oxygen would be purified, monitored and stored for use inside sealed, pressurised habitats, scientific facilities and potentially rocket systems. The carbon monoxide by-product must be safely isolated, managed or processed rather than introduced into occupied spaces.

One potential research location is **within Olympus Mons**, the giant Martian shield volcano, where excavated or otherwise engineered rock-covered facilities might offer shelter and radiation protection. This is a **site hypothesis**, not a demonstrated geological opportunity: subsurface stability, access, resources, contamination, heat rejection and construction feasibility would all need investigation. The summit's great altitude makes its already sparse atmospheric feedstock still thinner, a serious disadvantage for a carbon dioxide intake plant. Lower flanks, nearby terrain and lower-elevation sites should be compared before a location is selected.

The proposal demonstrates an important distinction in Evergence: making breathing oxygen for an enclosed community is a plausible future engineering application of demonstrated chemistry; making Mars's entire open atmosphere breathable is a vastly different task requiring much larger gas inventories, power resources and planetary-scale intervention. The scientific and ethical assessment must remain separate from any claim of authority to carry out an intervention.

## 1. Demonstrated chemical principle

A solid-oxide carbon dioxide electrolyser can carry out the net reaction:

$$
\boxed{2\mathrm{CO_2}\;\longrightarrow\;2\mathrm{CO}+\mathrm{O_2}}
$$

The reactor does **not create oxygen atoms**. It reorganises atoms present in the feed gas into molecular oxygen and carbon monoxide, consuming energy to do so. A simplified physical process is:

1. Gather Martian atmospheric gas (chiefly CO₂), remove dust and compress the feed.
2. Heat the gas and pass it through a solid-oxide electrolysis stack supplied with electrical power.
3. Separate and analyse the O₂ stream; condition, compress and store usable oxygen.
4. Handle CO and unused feed gases independently and prevent their entry to occupied habitats.
5. Blend stored O₂ with suitable inert diluent gas inside a pressurised habitat, with continuous life-support monitoring.

NASA's MOXIE experiment on the Perseverance rover produced **122 g of O₂ in total** over **16 experimental runs** by August 2023, achieving **up to 12 g/h** during its most productive operation at **at least 98% purity**. This demonstrated the chemical process, **not** continuous autonomous operation or a crew-rated installation [1].

## 2. Stoichiometric mass balance

Using molar masses 44 g/mol for CO₂, 28 g/mol for CO and 32 g/mol for O₂, production of **one kilogram of O₂** ideally requires:

$$
\boxed{m_{\mathrm{CO_2,consumed}}=\frac{88}{32}\,m_{\mathrm{O_2}}=2.75\,m_{\mathrm{O_2}}}
$$

and produces:

$$
\boxed{m_{\mathrm{CO,produced}}=\frac{56}{32}\,m_{\mathrm{O_2}}=1.75\,m_{\mathrm{O_2}}.}
$$

Thus, for each 1 kg of O₂, the reaction consumes 2.75 kg of CO₂ and creates 1.75 kg of CO. The sum of product masses equals the input mass, consistent with mass conservation. These are *reaction masses*, not total plant intake; unreacted feed, compression losses and inefficiencies add requirements.

Define $R(t)$ as the oxygen output rate (kg/s), $C(t)$ as crew consumption (kg/s) and $L(t)$ as leaks and other net losses (kg/s). For the combined usable O₂ inventory in habitat and storage:

$$
\boxed{\frac{dM_{\mathrm{O_2}}}{dt}=R(t)-C(t)-L(t)}
$$

where transfers between storage and habitat cancel within the combined inventory. Integration gives:

$$
\boxed{M_{\mathrm{O_2}}(t)=M_{\mathrm{O_2}}(t_0)+\int_{t_0}^{t}[R(s)-C(s)-L(s)]\,ds.}
$$

This is the first *Integration Up Level* (IUL) inventory calculation. The integration constant is the measured or specified initial oxygen mass, not new oxygen. A second integral of the inventory would have units **kg·s** and cannot be treated as additional oxygen production.

## 3. Worked four-person habitat example

For illustration, assume **four people**, a nominal oxygen use of **0.84 kg per person per Earth day**, no reclaimed oxygen credited and no plant downtime or leakage. This demand assumption is used in NASA-associated space life-support studies [2].

| Quantity | Ideal illustrative rate |
| --- | ---: |
| Four-person oxygen consumption | **3.36 kg O₂/day** |
| Net production needed, before reserve and losses | **0.140 kg O₂/hour** |
| CO₂ chemically consumed | **9.24 kg CO₂/day** |
| CO by-product requiring safe handling | **5.88 kg CO/day** |
| Continuous output compared with MOXIE's best measured hourly rate | **11.7 times** |

The last comparison is **not an estimate of how many flight MOXIE units would be suitable**, since MOXIE did not prove continuous service, reliability, equipment lifetime or crew safety. A real facility also needs storage reserves, duplicate critical equipment, planned maintenance with spares, gas purification, air scrubbing, inert buffer gases and independent power and monitoring. The calculation is in **Earth days**, rather than Martian sols.

## 4. Energy and safe breathable air

At the reference state of **298 K**, the standard Gibbs free-energy change for the half-reaction

$$\mathrm{CO_2\rightarrow CO+\tfrac12 O_2}$$

is approximately **257.18 kJ per mole of CO₂** [3]. The reference-state reversible work for the production of one mole of O₂ is twice that value, yielding approximately **4.47 kWh/kg O₂**. On that limited reference-state basis, the four-person example represents about **15 kWh/day** of reversible reaction work.

This is **not a plant power estimate**. The electrochemical free-energy requirement varies with operating temperature, pressure and gas composition. MOXIE-class solid-oxide systems run hot; the plant also needs compression, thermal management, processing, gas analysis, safety controls and storage; electricity and supplied thermal energy must be budgeted separately. An engineering calculation should instead use measured *system-specific energy consumption* $e_{\rm plant}$ in J/kg O₂:

$$
\boxed{P_{\rm plant}(t)\simeq R(t)\,e_{\rm plant}(t),}
$$

plus separately accounted standby, heating, storage and balance-of-plant loads if they are not already included in $e_{\rm plant}$.

**Oxygen is not, by itself, breathable air.** The habitat must have an appropriate overall pressure, oxygen *partial* pressure, gas mixture and carbon dioxide and contaminant limits. For an ideal, uniformly mixed habitat at temperature $T$ and internal volume $V$, the oxygen partial pressure is:

$$
\boxed{p_{\mathrm{O_2}}=\frac{M_{\mathrm{O_2}}}{0.032\;\mathrm{kg/mol}}\,\frac{R_gT}{V}.}
$$

For an illustrative 100 m³ sealed volume at 293 K and oxygen partial pressure 21 kPa, this gives about **27.6 kg of O₂ within the habitat gas mixture**. It does **not** specify the mass of nitrogen, argon or other suitable inert diluent required; nor is it a complete life-support design. NASA's human-spaceflight standards govern acceptable cabin atmosphere design, including oxygen toxicity, fire safety, carbon dioxide and minimum diluent requirements [4].

## 5. Could the reactor be inside Olympus Mons?

That is a legitimate **research hypothesis**, with competing considerations:

- **Possible benefit:** a purpose-built facility beneath suitable rock could gain shielding from radiation, temperature fluctuations and micrometeoroids. The existence of safe, accessible and stable natural cavities at a specific proposed site must **not** be assumed.
- **Critical disadvantage:** carbon dioxide is gathered from extremely thin air. NASA's simple upper-atmosphere pressure model predicts approximately **0.10 kPa** at a nominal altitude of 21 km, compared with roughly **0.6 to 0.7 kPa** near its reference level. This rough model is not a surveyed local pressure forecast. A summit plant would have markedly lower feed density and a harder compression and intake problem [5].
- **Other unresolved questions:** availability of water or extractable in situ materials, ability to construct safe access, handling CO, transport, dust filtration, long-term geological stability, power, heat rejection, communications, radiation and planetary protection.

The recommended wording is therefore **“a potential excavated or engineered reactor facility within or near Olympus Mons, to be compared against lower-elevation sites”** rather than choosing the summit as a settled design decision.

## 6. Why this is not yet global terraforming

NASA reports Mars's current atmospheric pressure near **6.36 mbar** at the mean radius, with the atmosphere overwhelmingly CO₂ [6]. Even the extreme and impractical thought experiment of converting *all currently available atmospheric CO₂* by the reaction above yields only a few millibars of O₂ partial pressure, around **2.3 mbar** under simplified assumptions. This is less than 2% of the roughly **210 mbar O₂ partial pressure** often used for comparison with Earth's sea-level atmosphere. Additional bulk gases, sourcing, heating and retention would therefore be necessary for global open-air habitability.

A 2026 analysis by Turyshev [7] finds that no surveyed abiotic global engineering pathway simultaneously satisfies all the atmosphere, temperature, industrial throughput, power, retention and operating constraints. This is why Evergence should keep the existing **three distinct scenarios**: enclosed habitats, covered regional habitats and speculative long-horizon global transformation.

## 7. Minimum requirements for an Evergence model

An initial computational demonstration should specify the initial gas inventories and external atmospheric supply; species mass balance and conserved elements; plant throughput; measured energy consumption; enclosure volume, pressure and temperature; crew oxygen use; CO₂ removal; buffer gas; leak and failure cases; seasonal site pressure; redundancy and reserves; provenance of all assumptions; and independent review of scientific and planetary protection concerns. The model must be able to **fail honestly** where conditions cannot be met.

## Sources

1. NASA (2023), [MOXIE completes Mars mission](https://www.nasa.gov/solar-system/nasas-oxygen-generating-experiment-moxie-completes-mars-mission/).
2. NASA technical report, [Mars transit oxygen requirements: 0.84 kg/person/day](https://ntrs.nasa.gov/api/citations/20170007268/downloads/20170007268.pdf?attachment=true).
3. Reichbauer et al. (2024), [CO₂-to-CO electrolysis and standard Gibbs energy](https://doi.org/10.1002/elsa.202300024).
4. NASA, [NASA-STD-3001: Human-system habitability and environmental standards](https://www.nasa.gov/reference/nasa-std-3001v2/).
5. NASA Glenn Research Center, [Mars atmosphere and altitude model](https://www1.grc.nasa.gov/beginners-guide-to-aeronautics/mars-atmosphere-equation-metric/).
6. NASA, [Mars Fact Sheet](https://nssdc.gsfc.nasa.gov/planetary/factsheet/marsfact.html?level=1).
7. S. G. Turyshev (2026), [Terraforming Mars: Mass, forcing and industrial throughput constraints](https://doi.org/10.1103/krb8-h3v3).
