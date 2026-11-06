---
layout: default
title: Updatez.org — Software for modern Macs
description: Useful software, renewed for macOS and Apple Silicon. Explore open-source projects, developer tools, and professional software porting services.
---
<section class="hero" aria-labelledby="intro-title">
  <p class="eyebrow">Legacy software. Modern possibilities.</p>
  <h1 id="intro-title">Useful tools.<br>Ready for modern Macs.</h1>
  <p class="hero-lead">Bringing trusted Windows and Unix software to macOS and Apple Silicon, with open-source tools and practical porting expertise.</p>
  <div class="actions">
    <a class="button" href="#software">Explore the software <span aria-hidden="true">↓</span></a>
    <a class="button button-secondary" href="https://github.com/{{ site.author.github }}">Find us on GitHub <span aria-hidden="true">↗</span></a>
  </div>
  <div class="hero-topics"><span>macOS &amp; Apple Silicon</span><span>Open-source development</span><span>Software porting</span></div>
</section>

<section id="software" aria-labelledby="software-title">
  <div class="section-heading"><p class="eyebrow">The toolkit</p><h2 id="software-title">Software worth bringing forward.</h2><p>Explore the projects, inspect the source, and support their continued development.</p></div>
  {% include project-cards.html %}
</section>

<section id="services" class="service-panel" aria-labelledby="services-title">
  <div>
    <p class="eyebrow">Software porting services</p>
    <h2 id="services-title">A new platform.<br>A practical path forward.</h2>
    <p>Move applications from Windows, Linux, and legacy Unix systems to modern macOS. Start with a technical feasibility evaluation covering source code, dependencies, platform compatibility, and the build system.</p>
    <a href="{{ '/pages/porting-process.html' | relative_url }}">Explore the porting process <span aria-hidden="true">→</span></a>
  </div>
  <div class="service-pricing">
    <h3>Porting evaluation</h3>
    <p class="price">$500 <span>flat rate</span></p>
    <p>A technical feasibility report outlining complexity, risks, and estimated engineering effort.</p>
    <p>Engineering after evaluation: <strong>$200 / hour</strong>.</p>
    <a class="button" href="mailto:stevenaedwards82@gmail.com">Discuss your project</a>
  </div>
</section>

<section id="case-studies" aria-labelledby="studies-title">
  <div class="section-heading"><p class="eyebrow">Behind the builds</p><h2 id="studies-title">Engineering in detail.</h2><p>Technical notes on bringing established tools to a new platform.</p></div>
  <ul class="study-list">
    <li><a href="{{ '/case-studies/MacDependency_White_Paper.pdf' | relative_url }}">MacDependency <span>White paper · PDF ↗</span></a></li>
    <li><a href="{{ '/case-studies/gftp_macos_gtk3_whitepaper.pdf' | relative_url }}">gFTP for macOS <span>White paper · PDF ↗</span></a></li>
    <li><a href="{{ '/case-studies/putty.html' | relative_url }}">PuTTY for macOS <span>Case study →</span></a></li>
    <li><a href="{{ '/case-studies/putty_macos_apple_silicon_whitepaper.pdf' | relative_url }}">PuTTY on Apple Silicon <span>White paper · PDF ↗</span></a></li>
    <li><a href="{{ '/case-studies/AppBundleGenerator_White_Paper_download.pdf' | relative_url }}">AppBundleGenerator <span>White paper · PDF ↗</span></a></li>
    <li><a href="{{ '/case-studies/rdesktop-mac-whitepaper.pdf' | relative_url }}">rdesktop-mac <span>White paper · PDF ↗</span></a></li>
  </ul>
</section>

<section id="support" class="support-panel" aria-labelledby="support-title">
  <p class="eyebrow">Keep useful software moving</p>
  <h2 id="support-title">Support the next build.</h2>
  <p>Your contributions help maintain the tools and bring more software to modern macOS. Explore the code, report an issue, or contribute to development.</p>
  <div class="actions">
    <a class="button" href="{{ site.support_url }}">Donate with PayPal <span aria-hidden="true">♡</span></a>
    <a class="button button-secondary" href="https://github.com/{{ site.author.github }}">Explore projects on GitHub <span aria-hidden="true">↗</span></a>
  </div>
</section>

<section id="contact" class="contact-panel" aria-labelledby="contact-title">
  <h2 id="contact-title">Let’s talk software.</h2>
  <p>Questions about software, licensing, or a porting project?</p>
  <a href="mailto:stevenaedwards82@gmail.com">stevenaedwards82@gmail.com</a>
</section>
