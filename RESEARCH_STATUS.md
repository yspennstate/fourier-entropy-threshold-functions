# Research status and proof boundaries

11 October 2026

## What is established in this manuscript

The threshold theorem covers every deterministic linear threshold function under the uniform input measure. No condition is imposed on weight size, arithmetic structure, margin, or threshold. The stronger class of regular Boolean functions is defined by a total desirability order.

The revised exact coefficient is

$$C_{\rm reg}=\log_2(4+e)+2\log_2(e\pi)<8.937.$$

Its proof uses three explicit estimates:

$$H(|\mathcal S|)\le\log_2(4+e)I(f),$$

$$\mathbb E_\nu\ln\frac r{|T\cap U|+1}\le\sum_{q=1}^{r-1}\frac{2^{-q}\binom q{\lfloor q/2\rfloor}}q\le1+\ln2,$$

and the Euler-product reference

$$Q_k(S)=\frac{(2k+1)!}{\pi^{2k}}\prod_{i\in S}i^{-2},\qquad |S|=k.$$

For multiple coordinate orders a separate Laplace-transform estimate is used. The single-order value $1+\ln2$ is **not** substituted into the multiple-order proof. The exponential tail used in the bounded-overlap theorem remains the original independently valid tail.

The product-measure theorem concerns symmetric thresholds. Arbitrary weighted thresholds at biased internal gates still require the hypotheses stated in the paper.

## The completed overlap continuation

The queue construction admits a reference probability for every successful finite witness. For each Fourier set, the revised statement minimizes the cost over assignments of its coordinates to gates and over valid directed forests. It retains the number of used gates, their overlap congestion, and their root probabilities.

For addressing on $m$ controls, a whole Fourier set uses one gate. The refined queue estimate gives $H(f)<10I(f)$ uniformly in $m$. The direct selector calculation gives the exact stronger statement

$$H(f)=2m=4[I(f)-1],\qquad I(f)=1+m/2.$$

The general selector theorem for arbitrary cell partitions requires balanced leaves with disjoint nonempty **Fourier supports**. The underlying leaf variable sets may overlap. Removing Fourier-support separation creates interference between coefficient contributions; the separate multiplexer result below treats that interference under a different explicit hypothesis.

## Shared-data extension after recovery

For a uniform selector $x\in\{-1,1\}^a$ and arbitrary Boolean branches $g_b$ on a common data cube, the paper now includes an exact entropy identity that retains collisions between their Fourier coefficients. It implies

$$H(g_x)\le2a+2^{-a}\sum_bH(g_b),\qquad I_{\rm data}(g_x)=2^{-a}\sum_bI(g_b).$$

If each neighboring pair satisfies $\mathbb E[g_bg_{b^{(j)}}]=0$, then $I_{\rm sel}(g_x)=a/2$. Thus a common branch FEI constant $C$ is preserved as $\max\{4,C\}$. Iterating with regular leaves gives the constant $C_{\rm reg}<8.937$, without a depth, fan-in or branch-data-overlap factor.

Every selector introduced at a node must be fresh and independent of all branches at that node, and neighboring-branch orthogonality must hold there under the common uniform data law. Branches need not be balanced or have disjoint Fourier supports. The result does not assert a universal entropy-increment bound in terms of selector influence.

This extension was incorporated after recovery of the interrupted draft. Its normalization, entropy chain rule, influence identities and recursive closure were independently audited. The shared-majority example has the exact values $H=3$ and $I=2$.

## What remains unresolved

No proof of the unrestricted Fourier entropy–influence conjecture is supplied. For the queue route, the missing estimate is a universal bound on the expected whole-witness cost, including normalization, rank, and sparse-root contributions, in terms of one influence budget.

The limitation can be stated exactly. For balanced arbitrary $g$,

$$M_g=\frac{1+g}{2}y_1+\frac{1-g}{2}y_2$$

satisfies

$$H(M_g)=2+\tfrac12H(g),\qquad I(M_g)=1+\tfrac12I(g).$$

Balancing tensor powers removes the additive terms. Hence a universal FEI bound for this two-cell selector class has exactly the same optimal constant as full FEI.

Likewise, sparsely activating balanced tensor powers produces functions with arbitrarily small influence and arbitrarily small probability of the minority output while preserving any original entropy-to-influence ratio in the limit. The paper credits earlier low-influence reductions and proves the exact identities used here.

The older parity-support and sparsely activated bent-function examples remain consistent with this outcome: they obstruct particular local entropy payments without refuting FEI. They do not become proofs of a universal bound by changing the accounting terminology.

## Review and computational scope

The revised rank argument, the original bounded-overlap argument, the biased symmetric-threshold proof, and the exact composition identities were analytically reviewed. The new queue, selector, shared-data multiplexer, and sparse-activation identities were separately checked. A fresh post-recovery audit found no gap in the all-LTF/regular proof, the biased symmetric-threshold proof, the composition conversions, or the shared-data extension. The paper's AI declaration describes the assistance; these reviews are not external peer review or proof-assistant certification.

The scripts retain exact integer or rational checks where the quantities are algebraic. Logarithmic entropy identities are checked numerically with stated tolerances. Their complete finite coverage and outputs are recorded in the accompanying JSON files. No enumeration is used to infer an all-dimensional theorem.

The principal qualitative contribution remains the all-threshold theorem and the structured extensions. The improved constant and joint-description results strengthen that contribution. Publication priority for the individual auxiliary identities is not asserted.

