---
layout: page
permalink: /research/
title: Research
nav: true
nav_order: 1
---

<style>
  .research-overview {
    margin-bottom: 2rem;
  }

  .research-overview p {
    margin-bottom: 0;
  }

  .research-area {
    background: #f6f8fa;
    border: 1px solid #e1e4e8;
    border-radius: 10px;
    padding: 1.5rem 2rem;
    margin-bottom: 1.75rem;
  }

  .research-area h3 {
    margin-top: 0;
    margin-bottom: 1rem;
  }

  .research-area h4 {
    margin-top: 1.5rem;
    margin-bottom: 0.75rem;
    font-size: 1.05rem;
  }

  .research-area .publications {
    margin-bottom: 0.5rem;
  }

  .research-area .see-all {
    margin: 0.75rem 0 0;
    font-size: 0.95rem;
  }

  /* Match al-folio's theme-aware cards in dark mode (as on Ricardo's site). */
  html[data-theme='dark'] .research-area {
    background-color: var(--global-card-bg-color);
    border-color: var(--global-divider-color);
  }

  @media (max-width: 768px) {
    .research-area {
      padding: 1.25rem;
    }
  }
</style>

<div class="research-overview">
  <p>My research interests are broadly on how machine-learning systems learn, adapt, and make decisions. My specific interests include continual learning, reinforcement learning, probabilistic methods/uncertainty quantification, and mechanistic interpretability.</p>
</div>

<section class="research-area">
  <h3>Continual Learning and Optimization</h3>

  <p>My MSc thesis at the University of Groningen focuses on <strong>optimization-based continual learning</strong> and is supervised by <a href="https://gmvandeven.github.io">Gido van de Ven</a> and <a href="https://www.linkedin.com/in/matthia-sabatelli-70370b93/">Matthia Sabatelli</a>.
    I am designing a new optimization framework based on proximal optimization for continual learning in a variety of scenarios (classification, reinforcement learning, etc.). I am currently in the process of finishing this by the end of the year and hope to share more soon :)
  </p>
</section>

<section class="research-area">
  <h3>Mechanistic Interpretability and Alignment</h3>

  <p>As a Research Fellow at <a href="https://apartresearch.com">Apart Research</a> (July 2025–March 2026), I co-authored <a href="https://arxiv.org/abs/2509.12934">The Anatomy of Alignment</a>, which uses interpretable sparse features to study preference optimization. We found that the learned policy favored style and formatting features over honesty-related ones, while generation coherence deteriorated. The paper received a <strong>Spotlight</strong> at the <a href="https://mechinterpworkshop.com/neurips2025/">NeurIPS 2025 Mechanistic Interpretability Workshop</a>.</p>

  <h4>Selected Papers</h4>

  <div class="publications">
    {% bibliography --group_by none --query @*[key=ferrao2025anatomy] %}
  </div>
  <p class="see-all"><a href="{{ '/publications/' | relative_url }}">See all publications &rarr;</a></p>
</section>

<section class="research-area">
  <h3>Reinforcement Learning and Probabilistic Methods</h3>

  <p>My bachelor's thesis was on <strong>interpretable function approximation with Gaussian processes</strong> in value-based model-free reinforcement learning. The work shows a practical way to use Gaussian processes in reinforcement learning. It was published at <a href="https://www.nldl.org/">NLDL 2025</a>.</p>

  <h4>Selected Papers</h4>

  <div class="publications">
    {% bibliography --group_by none --query @*[key=pmlr-v265-lende25a] %}
  </div>
  <p class="see-all"><a href="{{ '/publications/' | relative_url }}">See all publications &rarr;</a></p>
</section>
