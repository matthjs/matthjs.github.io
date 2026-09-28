---
layout: about
title: About
permalink: /
subtitle: University of Groningen · Groningen, Netherlands

profile: false
photo: /assets/DSCF6671.jpeg

selected_papers: false
social: false
announcements:
  enabled: false
latest_posts:
  enabled: false
---

<div class="row mb-3">
  <div class="col-sm-8" markdown="1">

I am currently a Master's student in Artificial Intelligence at the [University of Groningen](https://www.rug.nl/). My research interests center on how machine-learning systems learn, adapt, and make decisions, with a focus on continual learning, reinforcement learning, probabilistic methods, and mechanistic interpretability. I am interested in the limitations of machine learning methods and how these methods scale and behave as models grow larger.

Alongside my studies, I was a Research Fellow at [Apart Research](https://apartresearch.com/), where I worked on mechanistic interpretability. I have also been involved with [SAIN Groningen](https://safeainetherlands.org/chapters/groningen), including its discussion groups. I have taught and supervised student projects at the University of Groningen and completed internships in data science and machine learning at [Novigenix](https://novigenix.com/) and [Nuwa Innovation](https://nuwapen.com/).

I expect to graduate around January 2027 and am looking for a PhD position.

<!-- I am also interested in how these areas connect in foundation models. -->

<!--
Previously, I was a Research Fellow at [Apart Research](https://apartresearch.com), where I worked on mechanistic interpretability. Our collaborative paper, [The Anatomy of Alignment](https://arxiv.org/html/2509.12934v3), received a Spotlight at the [NeurIPS 2025 Mechanistic Interpretability Workshop](https://mechinterpworkshop.com/neurips2025/).
-->

  </div>
  <div class="col-sm-4">
    {% assign photo_path = page.photo %}
    {% include figure.liquid path=photo_path class="img-fluid z-depth-1 rounded profile-photo-square" width="240" height="240" alt="Profile photo" cache_bust=true %}
  </div>
</div>

<style>
  .contact-box {
    background-color: #f6f8fa;
    border: 1px solid #e1e4e8;
    border-radius: 10px;
    padding: 0.75rem 1.5rem;
    margin: 1.5rem 0 1.6rem;
    text-align: center;
  }

  .profile-photo-square {
    width: min(100%, 240px);
    height: auto;
    aspect-ratio: 1 / 1;
    object-fit: cover;
    object-position: center;
  }

  .contact-box p {
    margin: 0;
    text-align: center;
  }

  html[data-theme="dark"] .contact-box {
    background-color: var(--global-card-bg-color);
    border-color: var(--global-divider-color);
  }
</style>

<div class="contact-box" markdown="1">

**Contacts:** &nbsp; [matthijs.vanderlende@gmail.com](mailto:matthijs.vanderlende@gmail.com) &nbsp; \| &nbsp; [Google Scholar](https://scholar.google.com/citations?user=T4xxGdMAAAAJ) &nbsp; \| &nbsp; [OpenReview](https://openreview.net/profile?id=~Matthijs_van_der_Lende1) &nbsp; \| &nbsp; [GitHub](https://github.com/matthjs) &nbsp; \| &nbsp; [LinkedIn](https://www.linkedin.com/in/matthijs-van-der-lende-440b6426b/)

</div>

## News

<div class="news">
  <table class="table table-sm table-borderless">
    <tbody>
      <tr>
        <th scope="row" style="width: 20%">Aug, 2026</th>
        <td><strong>Aletheia's Quest:</strong> SAIN Groningen placed second in the black-box track of this LLM lie-detection competition and won the Scalability Award.</td>
      </tr>
      <tr>
        <th scope="row" style="width: 20%">May, 2026</th>
        <td><strong>Winner, AAMAS NS-Gym Competition:</strong> our PPO-based submission ranked first in all four evaluation criteria for agents adapting to non-stationary environments.</td>
      </tr>
      <tr>
        <th scope="row" style="width: 20%">Jan, 2026</th>
        <td>Recognized as an <strong>Outstanding Reviewer</strong> for NLDL 2026.</td>
      </tr>
      <tr>
        <th scope="row" style="width: 20%">Dec, 2025</th>
        <td><strong>Spotlight, NeurIPS 2025 Mechanistic Interpretability Workshop:</strong> our <a href="https://arxiv.org/abs/2509.12934">paper on interpretable feature steering for preference optimization</a> was presented as a spotlight.</td>
      </tr>
      <tr>
        <th scope="row" style="width: 20%">Jan, 2025</th>
        <td>Published first-author work on Gaussian-process function approximation for reinforcement learning at <strong>NLDL 2025</strong>. </td>
      </tr>
    </tbody>
  </table>
</div>

<h2><a href="{{ '/publications/' | relative_url }}" style="color: inherit">Publications</a></h2>

{% include selected_papers.liquid %}
