---
layout: page
permalink: /research/
title: Research
nav: true
nav_order: 1
---

<!--
  Each entry: title (+ coauthors in grey on the same line), one italic status line, one row of link buttons.
-->

## Working Papers

<div class="paper">
  <p class="paper-title">Grid-Lock: The Role of Backup Power in Reinforcing Electricity Outages</p>
  <p class="paper-links">
    <a href="#" class="abstract-toggle">Abstract</a>
    <!-- TODO: add the paper as assets/pdf/Wisniewska_GridLock.pdf (link 404s until then) -->
    <a href="{{ '/assets/pdf/Wisniewska_GridLock.pdf' | relative_url }}">PDF (Nov 2026)</a>
  </p>
  <div class="abstract-text" hidden>
    <!-- TODO: abstract -->
  </div>
</div>

<div class="paper">
  <p class="paper-title">Impacts and Cost-Effectiveness of Investments in Piped, Treated Water Provision <span class="paper-authors">with Rayan Sud</span></p>
  <p class="paper-status">Asian Development Bank Working Paper (forthcoming). Presented at the ADB Background Paper Workshop (2026).</p>
  <!-- TODO: add the slides as assets/pdf/Wisniewska_ADB_slides.pdf, then uncomment:
  <p class="paper-links">
    <a href="{{ '/assets/pdf/Wisniewska_ADB_slides.pdf' | relative_url }}">Slides</a>
  </p>
  -->
</div>

<div class="paper">
  <p class="paper-title">Power Struggles: The Gendered Employment Effects of Electricity Outages</p>
  <p class="paper-status">Undergraduate thesis, University of Cambridge. Presented at the <a href="https://bfi.uchicago.edu/news/three-uchicago-pre-doctoral-researchers-present-at-yale/">Yale Pre-Doctoral Economics Conference</a> and the <a href="https://iew2026.co.za/presenters/local-impacts-of-energy-infrastructure.html">International Energy Workshop</a>, University of Cape Town (2026).</p>
  <p class="paper-links">
    <a href="https://iew2026.co.za/presentations/Lena-Wisniewska_Power-Struggles-The-Gendered-Employment-Effects-of-Electrici.pdf">Slides</a>
  </p>
</div>

## Ongoing Projects

<div class="paper">
  <p class="paper-title">Long-run effects of school vouchers in Colombia <span class="paper-authors">(PIs: Eric Bettinger, Michael Kremer, Maurice Kugler, Carlos Medina, Christian Posso, and Juan E. Saavedra)</span><!-- TODO: confirm coauthorship before applications; if coauthor, switch back to "with ..." --></p>
  <p class="paper-status">Draft in preparation.</p>
</div>

<div class="paper">
  <p class="paper-title">Forecasting monsoon onset for Indian farmers <span class="paper-authors">with William R. Boos, Raju Mandal, Snehlata Tirkey, Deepeshkumar Jain, Susmitha Joseph, Colin Aitken, Haiyang Xiao, Rathan Sudheer, Anustup Biswas, and Shrabani Tripathy</span></p>
  <p class="paper-status">Abstract accepted at the <a href="https://studio.m-anage.com/agu/agu26/meetingapp.cgi/Paper/2069055">American Geophysical Union Annual Meeting</a> (2026). Draft in preparation.</p>
</div>

<div class="paper">
  <p class="paper-title">Willingness to pay for clean indoor air in Delhi schools <span class="paper-authors">(PIs: Guthrie Gray-Lobe, Sneha Nimmagadda, and Sabareesh Ramachandran)</span></p>
  <p class="paper-status">Funded; launching January 2027.</p>
</div>

<div class="paper">
  <p class="paper-title">Incentives for water chlorination in rural India</p>
  <p class="paper-status">Pilot stage.</p>
</div>

<script>
  // "Abstract" buttons show/hide the abstract under the same paper
  document.querySelectorAll(".abstract-toggle").forEach((link) => {
    link.addEventListener("click", (event) => {
      event.preventDefault();
      link.closest(".paper").querySelector(".abstract-text").toggleAttribute("hidden");
    });
  });
</script>
