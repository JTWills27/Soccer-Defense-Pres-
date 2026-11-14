---
layout: default
class: faq
routeAlias: faq
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Appendix · Backup slides</p>
  <h1>Mathematical Rigor: FAQ</h1>
</header>
<section class="faq-index" aria-label="Question index">
  <div>
    <p class="faq-group">Method choice</p>
    <Link to="faq-q1"><b>Q1</b><span>Why not plain Euclidean distance?</span></Link>
    <Link to="faq-q2"><b>Q2</b><span>Why z-score the variables first?</span></Link>
    <Link to="faq-q3"><b>Q3</b><span>What does Mahalanobis distance compute?</span></Link>
    <Link to="faq-q4"><b>Q4</b><span>What does eigendecomposing Σ give us?</span></Link>
    <Link to="faq-q5"><b>Q5</b><span>Why ZCA whitening, and does it matter?</span></Link>
    <Link to="faq-q6"><b>Q6</b><span>Why not z-score before whitening?</span></Link>
  </div>
  <div>
    <p class="faq-group">Numerical stability</p>
    <Link to="faq-q7"><b>Q7</b><span>Was the covariance matrix invertible?</span></Link>
    <Link to="faq-q8"><b>Q8</b><span>Why does the condition number matter?</span></Link>
    <Link to="faq-q9"><b>Q9</b><span>How was the matrix stabilized?</span></Link>
    <Link to="faq-q10"><b>Q10</b><span>Isn’t the 14-variable set arbitrary?</span></Link>
    <p class="faq-group">Verification &amp; interpretation</p>
    <Link to="faq-q11"><b>Q11</b><span>How do you know whitening worked?</span></Link>
    <Link to="faq-q12"><b>Q12</b><span>Can the two scores be compared?</span></Link>
    <Link to="faq-q13"><b>Q13</b><span>Is the year-gap effect significant?</span></Link>
    <Link to="faq-q14"><b>Q14</b><span>Does a low score mean similar teams?</span></Link>
  </div>
</section>
</main>

<!--
Backup slides; not part of the main talk. Click a question to jump to its answer. Every answer slide has an "FAQ index" link in the bottom-right corner to come back here.
-->

---
layout: default
class: faq
routeAlias: faq-q1
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q1 · Method choice</p>
  <h1>Why not just use plain Euclidean distance?</h1>
</header>
<section class="faq-cols">
<div class="faq-col">
  <div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">Correlated variables get counted more than once.</p></div>
  <div class="faq-body">
    <p>Euclidean distance adds up each variable’s gap independently. When two stats move together, the information they share enters the sum twice, and the formula never corrects for it.</p>
    <p>Whitening removes that shared variation first, so each independent direction of variation counts exactly once.</p>
  </div>
</div>
<div class="faq-card">

<h3>Correlation with Shots on Target</h3>

| Variable | Correlation |
|:--|--:|
| GK Clean Sheets | 0.563 |
| Clean Sheet % | 0.563 |
| Goals Allowed | −0.614 |
| Goals Allowed per 90 | −0.615 |
| GK Losses | −0.702 |

<p style="margin-top:.5rem">Goalkeeping stats correlate with an attacking stat at absolute values of 0.56–0.70. The overlap goes well beyond obvious pairs.</p>

</div>
</section>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
Euclidean distance treats every axis as independent, but soccer stats are heavily correlated. Table 2 of the paper shows goalkeeper variables correlating 0.56 to 0.70 in absolute value with shots on target. Correlated variables partly carry the same information, so Euclidean distance counts that information more than once.

Figure 2 in the paper illustrates the effect: Teams B and C are about equally far from A in Euclidean terms. B differs from A along the natural trend of the data, but C breaks the trend, so after whitening C is much farther away. Mahalanobis distance accounts for the covariance structure, so a difference along a common direction of variation counts for less than an unusual one.
-->

---
layout: default
class: faq
routeAlias: faq-q2
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q2 · Method choice</p>
  <h1>Why standardize the variables with z-scores first?</h1>
</header>
<section class="faq-cols">
<div class="faq-col">
  <div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">So every variable is on a comparable scale, and none dominates the distance just because its numbers are bigger.</p></div>
  <div class="faq-card">
    <h3>The z-score, step by step</h3>
    <div class="faq-steps">
      <div class="faq-step"><span class="faq-step-n">01</span><p>Subtract the variable’s mean from each observation.</p></div>
      <div class="faq-step"><span class="faq-step-n">02</span><p>Divide the result by that variable’s standard deviation.</p></div>
    </div>
    <p style="margin-top:.6rem">Every standardized variable then has a mean of 0 and a standard deviation of 1.</p>
  </div>
</div>
<div class="faq-col">
<div class="faq-card">
<h3>The Euclidean distance it feeds</h3>

<div class="faq-eq-sm">

$$
D=\sqrt{(a_1-b_1)^2+(a_2-b_2)^2+\cdots+(a_n-b_n)^2}
$$

</div>

With every entry a z-score, a wide-spread variable such as Passes Per Game no longer outweighs the others just because of its scale.

</div>
<div class="faq-caveat">
<span class="faq-label">What z-scores don’t fix</span>

They make the scales comparable but **don’t remove the relationships between variables**. That’s why the final score uses whitening.

</div>
</div>
</section>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
Section 5 of the paper: for the Euclidean-distance baseline, each variable is standardized with the z-score. Subtract the variable's mean from each observation, then divide by the variable's standard deviation. Each standardized variable has mean 0 and standard deviation 1, so variables with larger numerical spreads, such as Passes Per Game, don't influence the Euclidean distance more just because of their scale.

The paper's example: comparing shots on target for 2024/25 Tottenham and 2004/05 Middlesbrough, then repeating that for every variable to get an overall measure of similarity.

Key limitation, also from the paper: standardizing makes the scales comparable, but it doesn't remove the relationships between variables. That's the motivation for whitening and Mahalanobis distance. Standardization is used only for the Euclidean baseline.
-->

---
layout: default
class: faq
routeAlias: faq-q3
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q3 · Method choice</p>
  <h1>What does Mahalanobis distance actually compute?</h1>
</header>
<section class="faq-cols">
<div class="faq-col">
  <div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">Ordinary Euclidean distance, measured after the data have been whitened.</p></div>
<div class="faq-card">

Whiten every team-season vector with $\Sigma^{-\frac{1}{2}}$, then apply the same formula:

<div class="faq-eq-sm">

$$
D=\sqrt{(a_1-b_1)^2+(a_2-b_2)^2+\cdots+(a_n-b_n)^2}
$$

</div>

Here $(a_1,\dots,a_n)$ and $(b_1,\dots,b_n)$ are the **whitened** vectors of the two teams.

</div>
</div>
<div class="faq-card">
<h3>What whitening does to the data</h3>
<div class="faq-steps">
<div class="faq-step"><span class="faq-step-n">01</span><div>

**Center:** subtract each variable’s mean, so every variable has mean 0.

</div></div>
<div class="faq-step"><span class="faq-step-n">02</span><div>

**Rescale:** scale each principal direction by $\frac{1}{\sqrt{\lambda_i}}$, so its variance becomes $\lambda_i\left(\frac{1}{\sqrt{\lambda_i}}\right)^2=1$.

</div></div>
<div class="faq-step"><span class="faq-step-n">03</span><div>

**Decorrelate:** the covariance between different transformed variables is 0.

</div></div>
</div>
</div>
</section>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
Section 6 of the paper: Mahalanobis distance between two vectors can be thought of as the Euclidean distance after whitening. Whitening transforms the variables so they have variance 1 and are uncorrelated. In that whitened space, ordinary Euclidean distance can compare two team-seasons without overlapping information being counted multiple times.

The three properties the paper lists for whitened data: mean 0, variance 1 for each transformed variable, and covariance 0 between different transformed variables. Variance becomes 1 because each direction is scaled by one over the square root of its eigenvalue, and lambda i times that factor squared equals 1.
-->

---
layout: default
class: faq
routeAlias: faq-q4
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q4 · Method choice</p>
  <h1>What does the eigendecomposition of Σ give us?</h1>
</header>
<section class="faq-cols">
<div class="faq-col">
  <div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">Directions of variation (eigenvectors) and the variance along each (eigenvalues).</p></div>
<div class="faq-card">

$$
\Sigma = U\Lambda U^T
$$

**U:** its columns are Σ’s eigenvectors, the principal directions of variation. **U<sup>T</sup>:** the transpose of U. **Λ:** a diagonal matrix of Σ’s eigenvalues; each $\lambda_i$ is the variance along its direction.

</div>
</div>
<div class="faq-card">
<h3>One decomposition, four uses</h3>
<div class="faq-steps">
<div class="faq-step"><span class="faq-step-n">01</span><div>

**Whitening:** $\Sigma^{-\frac{1}{2}}=U\Lambda^{-\frac{1}{2}}U^T$ scales each direction by $\frac{1}{\sqrt{\lambda_i}}$.

</div></div>
<div class="faq-step"><span class="faq-step-n">02</span><div>

**Invertibility:** all the eigenvalues multiplied together give the determinant, so one near-zero $\lambda_i$ drives it toward 0.

</div></div>
<div class="faq-step"><span class="faq-step-n">03</span><div>

**Conditioning:** $\kappa(A)=\frac{\lambda_{\max}}{\lambda_{\min}}$ comes from the same eigenvalues.

</div></div>
<div class="faq-step"><span class="faq-step-n">04</span><div>

**Redundancy:** a very small $\lambda_i$ means very little variation in that direction, a sign of nearly redundant variables.

</div></div>
</div>
<p class="faq-stat-label" style="margin-top:.7rem">Final 14 × 14 matrix: eigenvalues from 4513 down to 0.6.</p>
</div>
</section>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
Section 6 of the paper expresses Sigma as U Lambda U transpose. The columns of U are Sigma's eigenvectors, the principal directions of variation in the data. U transpose is its transpose: rows become columns. Lambda is a diagonal matrix of Sigma's eigenvalues, the magnitude of the variance along each direction. Combined, they reconstruct Sigma and its variance and covariance structure.

The same decomposition does four jobs in the paper. It builds the whitening matrix, Sigma to the minus one half equals U Lambda to the minus one half U transpose. The eigenvalues multiplied together give the determinant, which is why the paper examined them when the determinant was about 10 to the minus 100. The condition number is the largest eigenvalue over the smallest. And a very small eigenvalue means very little variation in that direction, which can indicate nearly redundant variables.

The final 14 eigenvalues range from 4513 to 0.6 (Figure 4).
-->

---
layout: default
class: faq
routeAlias: faq-q5
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q5 · Method choice</p>
  <h1>Why ZCA whitening, and does the choice matter?</h1>
</header>
<section class="faq-cols">
<div class="faq-col">
  <div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">ZCA is the symmetric, covariance-based choice, and it keeps the 14 principal directions unchanged.</p></div>
<div class="faq-body">

The paper uses the Mahalanobis/ZCA whitening transformation, whose whitening matrix is $\Sigma^{-\frac{1}{2}}$ (Kessy et al., 2018).

$U$ and $U^T$ are unchanged, so the principal directions stay the same. Only how much the data is scaled along each direction changes.

</div>
</div>
<div class="faq-card">
<h3>How Σ<sup>−1/2</sup> is built</h3>
<div class="faq-steps">
<div class="faq-step"><span class="faq-step-n">01</span><div>

Eigendecompose: $\;\Sigma = U\Lambda U^T$

</div></div>
<div class="faq-step"><span class="faq-step-n">02</span><div>

Replace each $\lambda_i$ with $\lambda_i^{-\frac{1}{2}}=\frac{1}{\sqrt{\lambda_i}}$:

$$
\Lambda^{-\frac{1}{2}}=\begin{bmatrix}\frac{1}{\sqrt{\lambda_1}} & 0 & \cdots & 0\\ 0 & \frac{1}{\sqrt{\lambda_2}} & \cdots & 0\\ \vdots & \vdots & \ddots & \vdots\\ 0 & 0 & \cdots & \frac{1}{\sqrt{\lambda_{14}}}\end{bmatrix}
$$

</div></div>
<div class="faq-step"><span class="faq-step-n">03</span><div>

Rebuild: $\;\Sigma^{-\frac{1}{2}} = U\Lambda^{-\frac{1}{2}}U^T$

</div></div>
</div>
</div>
</section>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
The paper uses the Mahalanobis/ZCA whitening transformation, a symmetric covariance-based whitening whose whitening matrix is Sigma to the minus one half (references 6 and 7). It's built by eigendecomposition: write Sigma as U Lambda U transpose, replace each eigenvalue with one over its square root to get Lambda to the minus one half, and rebuild Sigma to the minus one half as U Lambda to the minus one half U transpose.

U and U transpose are unchanged, so the 14 principal directions are unchanged. Only how much the data is scaled in those directions changes.

If asked whether a different whitening method would change the scores: answer in words. Other whitening methods differ by a rotation of the whitened space, and rotations don't change Euclidean distances. This isn't stated in the paper; Kessy et al. (2018), reference 7, compares the whitening methods.
-->

---
layout: default
class: faq
routeAlias: faq-q6
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q6 · Method choice</p>
  <h1>Why z-score for Euclidean distance but not for whitening?</h1>
</header>
<section class="faq-cols">
<div class="faq-col">
  <div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">Whitening already accounts for scale. Z-scores are only needed for the Euclidean baseline.</p></div>
  <div class="faq-body">
    <p>Without z-scores, wide-spread stats like Passes Per Game would dominate the Euclidean distance.</p>
    <p>Whitening accounts for the scale of the variables <strong>as part of the transformation itself</strong>, so it’s applied to the final variables on their original, non-standardized scales.</p>
  </div>
</div>
<div class="faq-caveat">
  <span class="faq-label">Caveat worth raising yourself</span>
  <p>The condition numbers (10¹⁷ → 7,500) come from the covariance matrix on the variables’ <strong>original scales</strong>. Standardizing first could change the eigenvalues, and so the condition number.</p>
</div>
</section>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
Section 5 says the z-score standardization is used only for the Euclidean-distance baseline. The whitening procedure is applied to the final variables on their original, non-standardized scales, because whitening accounts for the scale of the variables as part of the transformation. Section 6 adds that the covariance matrices are calculated from the variables on their original scales.

The paper also notes that the condition number comes from a covariance matrix on the original scales, so standardizing beforehand could change the eigenvalues and the resulting condition number. Raise this before someone else does: the diagnostic depends on that choice.
-->

---
layout: default
class: faq
routeAlias: faq-q7
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q7 · Numerical stability</p>
  <h1>Was the original 40 × 40 covariance matrix invertible?</h1>
</header>
<div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">Mathematically, yes: the determinant isn’t zero. Numerically, no.</p></div>
<section class="faq-stats">
  <div class="faq-card"><span class="faq-label">Determinant</span><p class="faq-stat red">≈ 10<sup>−100</sup></p><p class="faq-stat-label">The product of all 40 eigenvalues</p></div>
  <div class="faq-card"><span class="faq-label">Largest λ</span><p class="faq-stat">6,175</p><p class="faq-stat-label">The main direction of variation</p></div>
  <div class="faq-card"><span class="faq-label">Smallest λ</span><p class="faq-stat red">~10<sup>−13</sup></p><p class="faq-stat-label">Directions with almost no variance</p></div>
  <div class="faq-card"><span class="faq-label">Negative λ</span><p class="faq-stat red">3</p><p class="faq-stat-label">As low as −3.2 × 10<sup>−13</sup></p></div>
</section>
<div class="faq-body"><p>A covariance matrix can’t truly have negative eigenvalues, so these values are rounding noise: those directions are <strong>numerically zero</strong>.</p></div>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
Figure 3 in the paper lists the 40 eigenvalues. The determinant is about 10 to the minus 100. It isn't zero, so the matrix is invertible in exact arithmetic, but the smallest eigenvalues are around 10 to the minus 13.

Three of them are slightly negative: minus 1.9e-14, minus 7.1e-14, and minus 3.2e-13. The paper doesn't point this out, but it strengthens the argument: a true covariance matrix can't have negative eigenvalues, so these values show the matrix is effectively singular in floating point. Some variables were near-exact linear combinations of others.
-->

---
layout: default
class: faq
routeAlias: faq-q8
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q8 · Numerical stability</p>
  <h1>Why does the condition number matter so much?</h1>
</header>
<section class="faq-cols">
<div class="faq-col">
  <div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">Whitening scales by 1/√λᵢ, so near-zero eigenvalues magnify noise and numerical error.</p></div>
<div class="faq-card">

$$
\kappa(A)=\frac{\lambda_{\max}}{\lambda_{\min}}
$$

R uses double-precision arithmetic, roughly 15–16 significant digits:

$$
\epsilon_{\text{machine}} \approx 2.2\times10^{-16}
$$

</div>
</div>
<div class="faq-col">
  <div class="faq-caveat">
    <span class="faq-label">Before pruning · 40 × 40</span>
    <p class="faq-stat red">κ(A) ≈ 10<sup>17</sup></p>
    <p>At that precision, even very small numerical errors could be greatly amplified. Far too ill-conditioned to whiten.</p>
  </div>
  <div class="faq-card">
    <span class="faq-label">After pruning · 14 × 14</span>
    <p class="faq-stat">κ ≈ 7,500</p>
    <p>Sufficiently well conditioned to support a stable whitening.</p>
  </div>
</div>
</section>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
The condition number is the largest eigenvalue over the smallest. As it approaches 1, the matrix is better conditioned and less sensitive to small numerical errors. Whitening scales each direction by one over the square root of its eigenvalue, so a near-zero eigenvalue makes that factor very large and magnifies noise or numerical error in that direction.

R uses double precision, roughly 15 to 16 significant digits, with machine epsilon about 2.2 times 10 to the minus 16. With a condition number around 10 to the 17, even extremely small numerical errors could be greatly amplified, so a direct whitening would be potentially unreliable. After pruning to 14 variables the condition number is about 7,500, which the paper judges well enough conditioned for a stable whitening.

The paper cites Moler and NIST for the condition number and the R documentation for machine epsilon.
-->

---
layout: default
class: faq
routeAlias: faq-q9
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q9 · Numerical stability</p>
  <h1>How was the covariance matrix made stable?</h1>
</header>
<div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">By removing near-redundant variables, recomputing κ after every removal.</p></div>
<section class="faq-pipe">
  <div class="faq-card"><h3>40 variables</h3><p class="faq-stat red">κ ≈ 10<sup>17</sup></p><p class="faq-stat-label">Every stat tracked 2000–2025</p></div>
  <div class="faq-arrow"><span>→</span>drop correlations of 0.99+</div>
  <div class="faq-card"><h3>21 variables</h3><p class="faq-stat">κ ≈ 330,000</p><p class="faq-stat-label">≈ 11 orders of magnitude better</p></div>
  <div class="faq-arrow"><span>→</span>drop correlations of 0.90+</div>
  <div class="faq-card final"><h3>14 variables</h3><p class="faq-stat">κ ≈ 7,500</p><p class="faq-stat-label">Eigenvalues from 4,513 down to 0.60</p></div>
</section>
<div class="faq-body"><p>A removal was kept only if it <strong>substantially lowered κ</strong>. Stopped at 14: with λ<sub>min</sub> = 0.60, further cuts would discard real information for diminishing gains.</p></div>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
Procedure from Section 6. Find groups of variables with absolute correlation of 0.99 or more. Within each group, remove a variable and recompute the condition number; keep the removal only if kappa drops substantially. The first pass brought kappa from about 10^17 down to about 330,000. A second pass at 0.90 removed 7 more variables, leaving 14 with kappa about 7,500 and eigenvalues from 4,513 down to 0.60.

Note: the paper doesn't state the variable count after the first pass; 21 is inferred from 14 plus the 7 removed in the second pass.
-->

---
layout: default
class: faq
routeAlias: faq-q10
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q10 · Numerical stability</p>
  <h1>Isn’t the final set of 14 variables arbitrary?</h1>
</header>
<section class="faq-cols">
<div class="faq-col">
  <div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">They were chosen for numerical stability, not importance, and the claims are scoped to match.</p></div>
  <div class="faq-body">
    <p><strong>Stop rule:</strong> with λ<sub>min</sub> = 0.60, more removals would discard real information for little gain in κ.</p>
    <p><strong>Known skew:</strong> 6 of 14 are goalkeeper stats, and some (Average Age, Players Used) describe the squad, not on-field play.</p>
  </div>
</div>
<div class="faq-card compact">

<h3>The 14 retained variables</h3>

| Goalkeeping + cards | Team &amp; squad |
|:--|:--|
| Clean Sheet % | Fouls |
| Save % | Total Players Used |
| Saves | Average Age |
| Shots on Target Faced | Total Substitutions |
| Ties | Minutes per Substitution |
| Goalkeepers Used | Penalties Attempted |
| Yellow Cards | Shots on Target per Game |

</div>
</section>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
Concede the point and explain the scoping. The 14 variables are what was left after removing redundancy that threatened the whitening. They weren't chosen as the 14 best descriptors of a team, and Section 6 says so. That's why the conclusion calls the score a measure of statistical-profile similarity and a proof of concept, not a measure of quality or playing style.

Possible follow-up: are 500 observations enough to estimate a 14 by 14 covariance? About 36 observations per variable is comfortable, though team-seasons from the same club aren't fully independent.
-->

---
layout: default
class: faq
routeAlias: faq-q11
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q11 · Verification</p>
  <h1>How do you know the whitening worked?</h1>
</header>
<section class="faq-cols">
<div class="faq-col">
  <div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">The whitened data’s covariance is the 14 × 14 identity, to three decimals.</p></div>
<div class="faq-caveat">
<span class="faq-label">What this does and doesn’t prove</span>

The whitening matrix is built from the same covariance matrix, so in exact arithmetic the identity is expected. The check shows the computation was **numerically stable**. It doesn’t show that the score measures anything meaningful.

</div>
</div>
<div class="faq-col" style="align-items:center">
  <svg viewBox="0 0 252 252" style="width:15rem;height:15rem" role="img" aria-label="14 by 14 grid with the diagonal filled, representing the identity matrix">
    <defs><pattern id="faq-grid" width="18" height="18" patternUnits="userSpaceOnUse"><rect width="18" height="18" fill="#ffffff" fill-opacity=".72" stroke="#e0dcd4" stroke-width="1"/></pattern></defs>
    <rect width="252" height="252" fill="url(#faq-grid)"/>
    <g fill="#c8102e">
      <rect x="1" y="1" width="16" height="16"/><rect x="19" y="19" width="16" height="16"/><rect x="37" y="37" width="16" height="16"/><rect x="55" y="55" width="16" height="16"/><rect x="73" y="73" width="16" height="16"/><rect x="91" y="91" width="16" height="16"/><rect x="109" y="109" width="16" height="16"/><rect x="127" y="127" width="16" height="16"/><rect x="145" y="145" width="16" height="16"/><rect x="163" y="163" width="16" height="16"/><rect x="181" y="181" width="16" height="16"/><rect x="199" y="199" width="16" height="16"/><rect x="217" y="217" width="16" height="16"/><rect x="235" y="235" width="16" height="16"/>
    </g>
    <rect width="252" height="252" fill="none" stroke="#282a2d" stroke-width="1.5"/>
  </svg>
  <p class="faq-stat-label" style="text-align:center"><code>round(whitened_cov, 3)</code>: 1 on the diagonal, 0 elsewhere; all means 0</p>
</div>
</section>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
Figure 5 in the paper shows R's output: the covariance of the whitened matrix, rounded to 3 decimals, is exactly the 14 by 14 identity.

Be careful how you claim this. When the whitening matrix is built from the same sample covariance, the result is the identity by algebra. So the check confirms a correct and numerically stable implementation, which matters given the earlier conditioning problem. It doesn't validate the score as a measure of similarity. Section 8 makes the same distinction: the identity check confirms the transformation; the changed distributions are descriptive consequences.
-->

---
layout: default
class: faq
routeAlias: faq-q12
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q12 · Interpretation</p>
  <h1>Can Euclidean and whitened scores be compared directly?</h1>
</header>
<section class="faq-cols wide">
<div class="faq-col">
  <div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">Not as raw numbers. They are distances in different spaces, so compare ranks or percentiles.</p></div>
<div class="faq-card">

| Space | Mean | SD | Min | Median | Max |
|:--|--:|--:|--:|--:|--:|
| Euclidean | 5.13 | 1.28 | 1.03 | 5.05 | 11.5 |
| Whitened | 5.10 | 1.02 | 1.20 | 5.07 | 10.7 |

<p style="margin-top:.5rem">Over all 124,750 pairs. The lower SD after whitening is descriptive; whitening doesn’t require it.</p>

</div>
</div>
<div class="faq-card">
  <h3>2019/20 Arsenal vs 2020/21 Burnley</h3>
  <span class="faq-label">Euclidean</span>
  <p class="faq-stat">5.31</p>
  <p class="faq-stat-label">More similar than 42.1% of pairs · “Moderately different”</p>
  <span class="faq-label" style="margin-top:.8rem">Whitened</span>
  <p class="faq-stat red">5.53</p>
  <p class="faq-stat-label">More similar than 32.4% of pairs · “Quite different”</p>
</div>
</section>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
Euclidean and whitened scores are lengths in two different coordinate systems, so a 5.3 in one isn't comparable to a 5.3 in the other. The paper says this in its discussion of Figure 11. The fair comparison is relative: ranks, nearest-neighbour lists, or the app's percentile mode.

Table 4 shows similar centers and a smaller spread after whitening, but the drop in spread isn't a requirement or a test of whitening. Example from Figure 10: Arsenal 2019/20 and Burnley 2020/21 change label from moderately different to quite different.
-->

---
layout: default
class: faq
routeAlias: faq-q13
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q13 · Interpretation</p>
  <h1>Is the year-gap effect statistically significant?</h1>
</header>
<section class="faq-cols">
<div class="faq-col">
  <div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">Treat it as descriptive: the 124,750 pairs aren’t independent.</p></div>
<div class="faq-body">

Each of the 500 team-seasons appears in 499 pairs, so the errors are correlated. The reported <code>p-value: &lt; 2.2e-16</code> overstates the evidence.

</div>
  <div class="faq-caveat">
    <span class="faq-label">If pressed for a test</span>
    <p>A permutation test that shuffles at the team-season level, or dyadic-cluster standard errors, would account for the dependence.</p>
  </div>
</div>
<div class="faq-card">

<h3><code>lm(formula = distance ~ year_gap, data = pairs)</code></h3>

| | Euclidean | Whitened |
|:--|--:|--:|
| Intercept | 4.353 | 4.834 |
| Slope per year | 0.094 | 0.043 |
| $R^2$ | 0.185 | 0.060 |

<p style="margin-top:.5rem">Seasons further apart are a bit less alike, but year gap explains ~18% of the variation before whitening and only ~6% after.</p>

</div>
</section>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
Figure 19 regresses pairwise distance on year gap. The slope is positive in both spaces. The paper already treats this as descriptive because the observations aren't independent: 500 choose 2 is 124,750 pairs, and each team-season appears in 499 of them, so the lm standard errors and p-values are too optimistic.

The test suggestions on the slide go beyond the paper; offer them as future work.
-->

---
layout: default
class: faq
routeAlias: faq-q14
---

<main class="faq-slide">
<header>
  <p class="faq-eyebrow">Q14 · Interpretation</p>
  <h1>Does a low score mean two teams played alike?</h1>
</header>
<div class="faq-short"><span class="faq-label">Short answer</span><p class="faq-answer">It means their 14-statistic profiles are close. Nothing more.</p></div>
<section class="faq-vs">
  <div class="faq-card"><span class="faq-label">Most similar to…</span><p class="faq-team">2003/04 Arsenal</p><p class="faq-stat-label">0 league losses all season</p></div>
  <div class="faq-vs-mid" aria-hidden="true">≈</div>
  <div class="faq-card"><span class="faq-label">…according to the score</span><p class="faq-team">2010/11 Everton</p><p class="faq-stat-label">10 league losses</p></div>
</section>
<div class="faq-body"><p>The distance is zero only when two 14-vectors are identical. Results, tactics and quality outside those 14 stats are invisible to it. Read the score as a proof of concept for comparing <strong>statistical profiles</strong>.</p></div>
<Link to="faq" class="faq-back">← FAQ index</Link>
</main>

<!--
The paper's own example from Section 8: Arsenal's unbeaten 2003/04 season was found most similar to Everton 2010/11, a team that lost 10 games. That isn't a bug. Wins and losses aren't among the 14 retained variables, so teams with very different results can still have close profiles in goalkeeping, discipline, squad and substitution stats. The paper concludes the score is a proof of concept for statistical-profile similarity, not a measure of team quality, playing style or future performance.
-->
