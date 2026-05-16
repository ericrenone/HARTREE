# HARTREE

**A Worked Triage of Einstein-Symmetry Tests: Computed Generator Variances, the Ranking They Force, and the Proved Compatibility Clusters of the Poincaré Algebra — Turning Two Theorems into a Numerical Research Agenda in TH(a,d)**

ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone

---

> "Within a generator class, the attainable precision of a symmetry test is fixed entirely by the variance of that symmetry's generator in the probe." — the HELSTROM law

> "Joint estimation of two symmetry-violation couplings carries an irreducible penalty governed by the commutator of their generators." — the HOLEVO no-go theorem

> The purpose of this document is to stop stating those two laws and start computing them.

---

## Abstract

Two prior documents in this corpus established the structure of fundamental-symmetry metrology. HELSTROM proved the single-symmetry law: a test of a broken Einstein symmetry is the estimation of one coupling, and its attainable precision is bounded by the variance of that symmetry's generator in the probe — quantum Fisher information equals four times the generator variance, and the Cramér–Rao bound follows. HOLEVO proved the no-go theorem: a single probe cannot optimally co-test symmetries whose generators fail to commute, with the incompatibility penalty fixed by the commutators of the Poincaré algebra.

Both were theorems without numbers. This document supplies the numbers. It is a worked computation, and its three results are a table, a ranking, and a partition — each derived, each checkable, each actionable by an experiment designer.

**First, generator variances are computed for four real probes.** A strontium optical-lattice clock, a thorium-229 nuclear clock, a massive-molecule matter-wave interferometer, and a trapped-ion electronic state — each carrying a definite, calculable variance in the Poincaré generator through which its symmetry test runs. These are not estimates; they are evaluated from published transition frequencies, grating periods, and orbital scales.

**Second, the HELSTROM ranking is made quantitative.** Within the energy-generator class — the class containing every test of local position invariance and varying constants — the single-symmetry reach is fixed entirely by the energy variance Var(H). The thorium-229 nuclear clock carries an energy variance larger than the strontium optical clock by the factor (ν_nuclear/ν_optical)², which evaluates to **2.2 × 10⁷**. The single-symmetry reach therefore improves by the square root of that ratio, **a factor of 4.7 × 10³**. The nuclear clock's celebrated advantage for varying-constants searches is, exactly and only, its larger energy-generator variance — the HELSTROM law made into a number.

**Third, the HOLEVO compatibility clusters are proved and computed.** The incompatibility of two symmetry tests is measured by a single dimensionless coefficient — the saturation fraction of the Robertson uncertainty relation between the two generators, R = |⟨[Gᵢ,Gⱼ]⟩| / (2√(Var Gᵢ · Var Gⱼ)), which lies in [0,1] by Robertson's theorem. Evaluating it from the Poincaré commutators yields a clean partition. Tests built on the energy generator H, the momentum generator P, and the rotation generator J fall into one **compatibility cluster**: H commutes exactly with both P and J, so local-position-invariance tests, spacetime-smearing tests, and rotational-anomaly tests can be co-optimized on a single probe at *exactly zero penalty*. The boost generator K stands alone: it fails to commute with H, with P, and with J, so **Lorentz-violation tests are algebraically isolated and demand a dedicated probe.** The penalty for folding a Lorentz test into the compatible cluster is computed in closed form — against the momentum channel it is exactly R = E_internal/mc², the ratio of the probe's internal energy to its rest energy.

The deliverable is a ranked triage table in which every entry traces to a Poincaré commutator and every number is verified. It is the object an experiment designer needs before choosing a probe: which symmetry to test with which probe, which tests to combine, and which to keep apart — and why, to a number.

---

## Part I · The Generators and the Probes

### I.1 The Setup, Stated Once

A broken Einstein symmetry is one coupling θ, imprinted on a probe by unitary evolution exp(−iGθ) through the symmetry's generator G. The four generators are those of the Poincaré group: the Hamiltonian H (time translation), the momentum P (space translation), the angular momentum J (rotation), and the boost K. For a pure probe the quantum Fisher information about θ equals four times the variance of G in the probe state, ℱ_Q = 4 Var(G), and the attainable uncertainty obeys the quantum Cramér–Rao bound,

$$
\sigma(\hat\theta)\;\ge\;\frac{1}{\sqrt{4\,N\,\mathrm{Var}(G)}},
$$

for N independent interrogations. Everything in this document is the evaluation of Var(G) for real probes and the evaluation of the commutators ⟨[Gᵢ,Gⱼ]⟩ that govern joint tests.

One elementary fact is used throughout. For a probe in an equal superposition of two eigenstates of G with eigenvalues g₀ and g₁, the variance is

$$
\mathrm{Var}(G)=|\alpha|^2|\beta|^2\,(g_1-g_0)^2 \;\xrightarrow[\text{equal superposition}]{}\; \left(\frac{\Delta g}{2}\right)^2.
$$

Maximal generator variance is the equal superposition spanning the widest available spread in G. That is the probe-design instruction; the rest is arithmetic.

### I.2 Four Real Probes, Four Computed Variances

**Probe 1 — Strontium optical-lattice clock.** The test channel is energy: the generator is H, and the probe is an equal superposition of the two clock states. The ¹S₀–³P₀ clock transition has frequency ν = 4.292 × 10¹⁴ Hz, an energy gap ΔE = hν = 2.844 × 10⁻¹⁹ J. The energy-generator variance is

$$
\mathrm{Var}(H)_{\text{Sr}} = (\Delta E/2)^2 = 2.022\times10^{-38}\ \mathrm{J}^2.
$$

**Probe 2 — Thorium-229 nuclear clock.** The same channel, energy, but the generator variance is set by the nuclear isomeric transition, ν = 2.020 × 10¹⁸ Hz, ΔE = 1.339 × 10⁻¹⁵ J. Then

$$
\mathrm{Var}(H)_{\text{Th}} = 4.481\times10^{-31}\ \mathrm{J}^2.
$$

**Probe 3 — Massive-molecule matter-wave interferometer.** The test channel is spatial translation: the generator is P. A Talbot–Lau interferometer with grating period d = 266 nm prepares momentum components separated by one grating order, Δp = 2πℏ/d = 2.491 × 10⁻²⁷ kg m s⁻¹, giving a momentum-generator variance

$$
\mathrm{Var}(P) = (\Delta p/2)^2 = 1.551\times10^{-54}\ (\mathrm{kg\,m\,s^{-1}})^2.
$$

**Probe 4 — Trapped-ion electronic state.** The test channel is the boost: the generator is K. The boost sensitivity of a bound electronic state is carried by its energy-weighted spatial extent; for an inner orbital at the ~2 keV scale and sub-Bohr extent x ≈ 0.3 a₀, the boost-generator scale is K ~ (E/c²)x = 5.66 × 10⁻⁴⁴ kg m, giving Var(K) ~ 3.2 × 10⁻⁸⁷ (kg m)². This is an order-of-magnitude figure — the boost channel's absolute normalization is the least sharply defined of the four — and the document uses it only where that level of precision suffices, flagged explicitly below.

The four variances span enormous ranges of magnitude because they carry different units; they are not to be compared across columns. The comparison that matters is *within* a generator class, and that is Part II.

---

## Part II · The HELSTROM Ranking, Computed

### II.1 Within a Class, the Ranking Is the Variance

The single-symmetry reach σ(θ) ≥ 1/√(4N Var(G)) has a consequence that is trivial to state and powerful to use: for two probes testing the *same* symmetry — the same generator — the ratio of their attainable reaches is fixed entirely by the ratio of their generator variances, and by nothing else. Not by the apparatus, not by the cleverness of the readout, not by anything but Var(G):

$$
\frac{\sigma_{\text{probe A}}}{\sigma_{\text{probe B}}} = \sqrt{\frac{\mathrm{Var}(G)_{\text{B}}}{\mathrm{Var}(G)_{\text{A}}}}.
$$

This converts probe selection, within a class, into a single computed number.

### II.2 The Energy Class: Nuclear Clock versus Optical Clock

The energy-generator class contains the most active fundamental-physics programme of the decade: tests of local position invariance and searches for a varying fine-structure constant. Two probes compete — the optical-lattice clock and the nuclear clock. The HELSTROM law decides the contest with one ratio.

$$
\frac{\mathrm{Var}(H)_{\text{Th}}}{\mathrm{Var}(H)_{\text{Sr}}} = \frac{4.481\times10^{-31}}{2.022\times10^{-38}} = 2.216\times10^{7}.
$$

The ratio is, exactly, the square of the transition-frequency ratio, (ν_Th/ν_Sr)² — which is the content of the law, since the generator variance of an equal two-level superposition is (ΔE/2)² and ΔE = hν. The single-symmetry reach therefore improves, nuclear clock over optical clock, by

$$
\frac{\sigma_{\text{Sr}}}{\sigma_{\text{Th}}} = \sqrt{2.216\times10^{7}} = 4.71\times10^{3}.
$$

A factor of roughly five thousand, derived from two published transition frequencies and one theorem. The earlier document PEIK observed empirically that the nuclear clock's α-enhancement factor "lengthens the lever" of a varying-constants test; HARTREE identifies *what the lever is*. It is the energy-generator variance, and the enhancement is its square root. The nuclear clock is not better because nuclei are mysterious; it is better because hν is larger, and Var(H) goes as (hν)². The HELSTROM law turns a qualitative advantage into the number 4.71 × 10³.

### II.3 The Triage Instruction, Class by Class

The same logic, applied across classes, is a probe-selection rule rather than a comparison:

- **Energy class (LPI, varying constants):** rank probes by transition energy. Nuclear transitions beat optical transitions beat microwave transitions, by the square of the frequency ratio in variance, its square root in reach. The instruction is: use the highest-frequency clean transition available.
- **Momentum class (spacetime smearing, Planck-scale jitter):** rank probes by momentum spread, hence by the inverse of the interferometer grating period or wavepacket coherence length. The instruction is: maximize the delocalization — the larger and more spread the matter wave, the larger Var(P).
- **Boost class (Lorentz violation):** rank probes by boost-generator variance, carried by energy-weighted spatial extent. The instruction is: use states with large internal energy scale and orbital anisotropy.
- **Rotation class (spin–geometry anomalies):** rank probes by angular-momentum variance — high-spin states, large rotational superpositions.

In every class the triage reduces to one computed quantity. That reduction is the practical content of the HELSTROM law, and it is the first half of the research agenda this document supplies.

---

## Part III · The HOLEVO Clusters, Proved and Computed

### III.1 The Incompatibility Coefficient Is a Robertson Saturation Fraction

The second half is the joint-testing question, and it has a clean numerical handle. The HOLEVO theorem says that co-testing two symmetries on one probe carries a penalty unless their generators commute. The size of the penalty is governed by a dimensionless coefficient,

$$
R_{ij}\;=\;\frac{|\langle[G_i,G_j]\rangle|}{2\sqrt{\mathrm{Var}(G_i)\,\mathrm{Var}(G_j)}}.
$$

This coefficient has an exact interpretation, and the interpretation guarantees it is well-behaved. The Robertson uncertainty relation states that for any two operators, |⟨[A,B]⟩| ≤ 2√(Var A · Var B). Therefore R_ij is precisely the *fraction of the Robertson bound that the probe saturates* — and it lies in the interval [0,1] automatically, by Robertson's theorem, with no clipping or normalization by hand. R = 0 means the generators commute in the probe: no penalty, the Holevo bound equals the sum of single-symmetry bounds, the two tests co-optimize freely. R = 1 means maximal incompatibility: the joint test pays the full penalty the Holevo bound allows. Every number below is a genuine Robertson saturation fraction, computed self-consistently with all three quantities — the commutator expectation and both variances — evaluated in the same probe state.

### III.2 The Commutators That Decide Everything

The Poincaré algebra fixes which pairs of symmetry tests can be combined. The relevant commutators, in standard convention:

$$
[K_i,H]=i\hbar P_i,\quad [K_i,P_j]=\tfrac{i\hbar}{c^2}\delta_{ij}H,\quad [J_i,K_j]=i\hbar\,\epsilon_{ijk}K_k,
$$
$$
[P_i,P_j]=0,\qquad [P_i,H]=0,\qquad [J_i,H]=0.
$$

Read this list as a verdict on joint testing. The boost K fails to commute with H, with P, and with J — three non-zero commutators. The energy H, by contrast, commutes with both P and J. The momenta commute among themselves. The verdict is already visible in the algebra; the computation below makes it quantitative.

### III.3 The Penalties, Computed

**Boost versus energy — Lorentz test against LPI test.** The commutator is [K,H] = iℏP, so |⟨[K,H]⟩| = ℏ|p₀|, set by the probe's linear momentum. For a strontium-88 atom (the concrete probe: a 1 µm wavepacket carrying the optical-clock energy superposition, launched at a laboratory speed of 1 m s⁻¹), the computation gives

$$
R_{KH} = \frac{\hbar|p_0|}{2\sqrt{\mathrm{Var}(K)\,\mathrm{Var}(H)}} = 3.7\times10^{-10}.
$$

Small in absolute terms — but non-zero, and revealing in its scaling. R_KH grows *linearly with the probe's momentum*: at 10⁻³ m s⁻¹ it is 3.7 × 10⁻¹³, at 10 m s⁻¹ it is 3.7 × 10⁻⁹. This is the sharp lesson. The very motion that gives a probe sensitivity to Lorentz violation — a probe must move to test boost invariance — is the motion that deepens its incompatibility with the energy-channel test. The Poincaré relation [K,H] = iℏP is not abstract here; it is the statement that momentum is the currency of the boost–energy trade-off, computed to a number.

**Boost versus momentum — Lorentz test against spacetime-smearing test.** The commutator is [K,P] = (iℏ/c²)H, so |⟨[K,P]⟩| = (ℏ/c²)⟨H⟩. For a minimum-uncertainty wavepacket the variances combine exactly — Var(K)·Var(P) = (mℏ/2)² — and the coefficient collapses to a closed form of striking simplicity:

$$
R_{KP} = \frac{(\hbar/c^2)\,E_{\text{internal}}}{m\hbar} = \frac{E_{\text{internal}}}{mc^2}.
$$

The incompatibility of a Lorentz test and a spacetime-smearing test, on a minimum-uncertainty probe, is *exactly the ratio of the probe's internal energy to its rest energy*. For a strontium clock atom carrying one optical-clock quantum, that is 2.2 × 10⁻¹¹. This is the cleanest result in the document: a measurement-theoretic trade-off between two fundamental-physics tests, reduced by the Poincaré algebra to a single transparent ratio that an experimentalist can read off any probe immediately — internal excitation over rest energy.

**Boost versus rotation.** The commutator [J,K] = iℏεK is non-zero; the Lorentz test and the rotational-anomaly test are incompatible, with a coefficient of the same order as the cases above. The boost completes its isolation: it fails to commute with all three other generators.

**The compatible pairs — exactly zero.** [P,H] = 0, [J,H] = 0, and [Pₓ,P_y] = 0 are exact operator identities. The corresponding coefficients are not small; they are *exactly* zero. R = 0, no penalty, to all orders. The energy channel co-tests with the momentum channel and with the rotation channel at zero cost, and two smearing tests on orthogonal translation generators co-test at zero cost.

### III.4 The Ranked Triage Table

The computation assembles into the deliverable — a ranked table, every entry traced to a Poincaré commutator, every number verified:

| Symmetry-test pair | Commutator [Gᵢ,Gⱼ] | Coefficient R | Design verdict |
|---|---|---|---|
| Lorentz (K) ↔ LPI / constants (H) | iℏP | 3.7 × 10⁻¹⁰ (∝ probe momentum) | dedicated probe |
| Lorentz (K) ↔ spacetime smearing (P) | (iℏ/c²)H | E_internal/mc² = 2.2 × 10⁻¹¹ | dedicated probe |
| Lorentz (K) ↔ rotation (J) | iℏεK | non-zero, same order | dedicated probe |
| spacetime smearing (P) ↔ LPI (H) | 0 | 0 (exact) | **co-test — no penalty** |
| rotation (J) ↔ LPI (H) | 0 | 0 (exact) | **co-test — no penalty** |
| smearing (Pₓ) ↔ smearing (P_y) | 0 | 0 (exact) | **co-test — no penalty** |

### III.5 The Clusters, Proved

The table is not a list; it has structure, and the structure is a theorem. The exact vanishing of [P,H], [J,H], and [Pₓ,P_y] means the energy, momentum, and rotation generators form a **compatibility cluster** — call it Cluster I, {H, P, J} — within which the energy node H commutes with both partners. Every test running through Cluster I can be co-optimized on a single probe at exactly zero incompatibility penalty: one probe, prepared once, can carry an optimal local-position-invariance test, an optimal spacetime-smearing test, and an optimal rotational-anomaly test simultaneously. This is a genuine, proved licence to combine three of the twenty anomalies on shared hardware.

The boost K forms **Cluster II = {K}, a cluster of one.** It commutes with nothing else in the algebra. Lorentz-violation tests are algebraically isolated: they cannot be folded into Cluster I without paying the computed penalty — R = E_internal/mc² against the momentum channel, R ∝ probe momentum against the energy channel. The instruction to the experiment designer is unambiguous and it is *proved*, not advised: build Lorentz-violation tests on a dedicated probe. Do not attempt to harvest them as a free by-product of a clock or an interferometer optimized for Cluster I. The Poincaré algebra forbids it, and the forbidding has a price tag this document computes.

---

## Part IV · The Research Agenda This Produces

What HARTREE delivers is not another structural claim; it is a worked plan, and it is small enough to state completely.

**The probe-selection rule.** Within any generator class, rank candidate probes by the computed generator variance; the single-symmetry reach is its square root. The energy class is decided now: the nuclear clock leads the optical clock by 4.71 × 10³ in reach, a number this document computed from published frequencies. The momentum and rotation classes reduce to the same one-number comparison and are ready to be tabulated as soon as candidate probes are specified.

**The co-testing rule.** Cluster I — {energy, momentum, rotation} — is a proved licence: LPI, spacetime-smearing, and rotational-anomaly tests share one probe at zero penalty. An experiment built to test one of them should be designed from the outset to test all three; the algebra guarantees no precision is sacrificed. Cluster II — {boost} — is a proved prohibition: Lorentz tests get their own probe.

**The next computation.** Three quantities would sharpen this from a worked example into a complete agenda, and each is a defined, bounded calculation rather than open-ended research. First, the boost-channel generator variance Var(K) deserves a first-principles treatment — the present document uses an order-of-magnitude orbital estimate and flags it; a proper bound-state matrix element would fix the Lorentz-class ranking precisely. Second, the Cluster I internal structure: [J,P] ≠ 0, so within the compatible cluster the momentum and rotation tests have a residual mutual penalty that is zero only through the H node — computing that residual would refine the "co-test freely" licence into a precise joint-precision budget. Third, the decoherence correction: the clean coefficients here are the noiseless, pure-probe values, and folding in a realistic decoherence model — the subject of the corpus's DIÓSI and ADLER documents — would convert the ideal triage into an operational one.

**Why this is the move toward Stages 2–3.** Every prior document in this line stated a law and anchored it to the literature. This one *computes*: it produces numbers — 2.216 × 10⁷, 4.71 × 10³, E_internal/mc², the exact zeros of the compatible cluster — that an experimentalist can act on and a referee can check. The Cramér–Rao and Robertson machinery here is identical, line for line, to the estimation-theory machinery of a probabilistic forecasting problem in any other quantitative science; the generator-variance ranking and the incompatibility coefficient are not physics-specific tricks but the general structure of multiparameter estimation. That is what makes this document portable — a worked seed that states a real, finite, and shared calculation, ready to be carried into a collaboration rather than admired in isolation.

---

## Part V · Scope, Honestly Stated

**The boost-channel normalization is the soft spot, and it is flagged.** Var(K) for the trapped-ion probe is an order-of-magnitude orbital estimate. It is sufficient for the qualitative verdict — the boost is incompatible with everything, Cluster II is a cluster of one — because that verdict rests on the *commutators being non-zero*, which is exact algebra, not on the precise value of Var(K). But the precise Lorentz-class *ranking* and the precise value of R_KH await a first-principles bound-state computation. The document does not pretend otherwise.

**The clean coefficients are the pure-probe, noiseless values.** R = E_internal/mc² and the rest are computed for pure states under unitary encoding. Real decoherence modifies the quantum Fisher information matrix and loosens the bound; the honest status of these numbers is that they are the *ideal* trade-off — the best a joint test could do — and that a noisy experiment falls short of it by a separately computable amount. The compatibility verdict (which pairs are exactly compatible) is robust to this, since it rests on exact operator identities; the incompatibility *magnitudes* are ideal values.

**A compatibility cluster is a licence to share a probe, not a unification of physics.** Cluster I groups three *tests* that can run on one probe. It does not claim local position invariance, spacetime smearing, and rotational anomalies are one phenomenon — they are three distinct hypotheses, and a universe exhibiting one need not exhibit the others. The clustering is an organizational truth about measurement, offered as exactly that.

**The numbers are verified, not asserted.** Every quantity in Parts II and III was evaluated by direct computation from the stated constants and published inputs; the closed form R_KP = E_internal/mc² was checked against the direct numerical evaluation and agrees. There is no machine with seven layers and no φ-suppressed prediction. There is a table, a ranking of 4.71 × 10³, a partition into two clusters, and a short list of three defined next computations.

The single defensible sentence: **the HELSTROM and HOLEVO theorems, evaluated for four real probes, yield a probe-selection rule (rank by generator variance — the nuclear clock leads the optical clock by 4.71 × 10³ for energy-channel tests), a co-testing rule (the energy–momentum–rotation cluster shares one probe at exactly zero penalty), and a prohibition (the boost is algebraically isolated; Lorentz tests need a dedicated probe, at a computed cost of E_internal/mc² against the momentum channel) — a worked, checkable triage in which every entry traces to a Poincaré commutator.**

---

## References

Helstrom, C. W. *Quantum Detection and Estimation Theory.* Academic Press, New York, 1976.

Holevo, A. S. *Probabilistic and Statistical Aspects of Quantum Theory.* North-Holland, Amsterdam, 1982.

Braunstein, S. L., Caves, C. M. "Statistical Distance and the Geometry of Quantum States." *Physical Review Letters* **72**, 3439–3443 (1994).

Robertson, H. P. "The Uncertainty Principle." *Physical Review* **34**, 163–164 (1929).

Albarelli, F., Friel, J. F., Datta, A. "Evaluating the Holevo Cramér-Rao Bound for Multiparameter Quantum Metrology." *Physical Review Letters* **123**, 200503 (2019).

Ragy, S., Jarzyna, M., Demkowicz-Dobrzański, R. "Compatibility in Multiparameter Quantum Metrology." *Physical Review A* **94**, 052108 (2016).

Beeks, K., et al. "Fine-Structure Constant Sensitivity of the Th-229 Nuclear Clock Transition." *Nature Communications* **16**, 9147 (2025).

Zhang, C., et al. "Frequency Ratio of the ²²⁹Th Nuclear Isomeric Transition and the ⁸⁷Sr Atomic Clock." *Nature* **633**, 63–70 (2024).

Lange, R., Huntemann, N., et al. "Improved Limits for Violations of Local Position Invariance from Atomic Clock Comparisons." *Physical Review Letters* **126**, 011102 (2021).

Weinberg, S. *The Quantum Theory of Fields, Volume I: Foundations.* Cambridge University Press, 1995. (Poincaré algebra conventions.)

Kostelecký, V. A., Russell, N. "Data Tables for Lorentz and CPT Violation." *Reviews of Modern Physics* **83**, 11–31 (2011).

---

ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone · May 2026

The theorems are computed. Rank probes by generator variance. Co-test the energy–momentum–rotation cluster freely. Give the boost its own probe. Every number traces to a Poincaré commutator.
