---
layout: page
title: Research
permalink: /research/
---

<style>
  .research-intro { text-align: center; margin-bottom: 60px; color: #555; font-size: 1.1em; max-width: 800px; margin-left: auto; margin-right: auto; }
  
  /* Flexbox Layout for the Z-Pattern */
  .research-row { display: flex; align-items: center; gap: 40px; margin-bottom: 80px; }
  .research-row.reverse { flex-direction: row-reverse; }
  
  .research-text { flex: 1; }
  .research-title { color: #222; margin-top: 0; border-bottom: 2px solid #eaeaea; padding-bottom: 10px; margin-bottom: 20px; font-size: 1.6em; }
  .research-description { line-height: 1.7; color: #444; margin-bottom: 25px; }
  
  /* Portrait Image Styling (3:4 ratio) */
  .research-img-container { flex: 0 0 40%; max-width: 400px; }
  .research-img { width: 100%; aspect-ratio: 3 / 4; object-fit: cover; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.1); transition: transform 0.3s ease; }
  .research-img:hover { transform: translateY(-5px); }
  
  /* Button Styles */
  .action-button { display: inline-flex; align-items: center; gap: 8px; background-color: #0A66C2; border: none; padding: 10px 20px; border-radius: 6px; text-decoration: none; color: white !important; font-weight: bold; transition: all 0.2s; box-shadow: 0 2px 5px rgba(0,0,0,0.15); }
  .action-button:hover { background-color: #004182; transform: translateY(-2px); box-shadow: 0 4px 10px rgba(0,0,0,0.2); }
  
  .badge-ongoing { display: inline-block; background-color: #e8f0fe; color: #1967d2; font-weight: bold; padding: 8px 16px; border-radius: 20px; font-size: 0.9em; }

  /* Expandable Publication List */
  details.pub-list { background-color: #fcfcfc; border: 1px solid #eaeaea; border-radius: 8px; padding: 12px 20px; margin-top: 15px; box-shadow: 0 2px 5px rgba(0,0,0,0.02); }
  details.pub-list summary { font-weight: bold; cursor: pointer; outline: none; color: #222; display: flex; align-items: center; }
  details.pub-list summary::before { content: "📚"; margin-right: 10px; }
  
  .pub-items { margin: 15px 0 0 0; padding-left: 20px; line-height: 1.8; }
  .pub-items li { margin-bottom: 10px; }
  .pub-items a { color: #0A66C2; text-decoration: none; font-weight: 500; }
  .pub-items a:hover { text-decoration: underline; }

  /* Mobile Responsiveness: Stack columns vertically on small screens */
  @media (max-width: 768px) {
    .research-row, .research-row.reverse { flex-direction: column; text-align: left; gap: 20px; margin-bottom: 60px; }
    .research-img-container { flex: 1; width: 100%; max-width: 100%; }
    .research-img { aspect-ratio: 16 / 9; /* Switch to landscape on mobile to save vertical space */ }
  }
</style>

<div class="research-intro">
  <p>My research is driven by the intersection of advanced deep learning architectures, computational efficiency, and real-world imaging systems. Below are the three primary vertices of my current academic focus.</p>
</div>

<div class="research-row">
  <div class="research-img-container">
    <img src="/assets/sar_research.webp" alt="Synthetic Aperture Radar Imaging" class="research-img">
  </div>
  
  <div class="research-text">
    <h2 class="research-title">Earth Imaging with Synthetic Aperture Radar (SAR)</h2>
    <div class="research-description">
      <p>Synthetic Aperture Radar (SAR) provides a profound advantage in Earth observation through its capability for 24/7 active imaging, regardless of weather or daylight. However, the sheer volume of data generated presents a significant transmission bottleneck.</p>
      <p>My work focuses on designing an optimal model to downstream only the novel aspects of SAR-data tiles. To achieve this, we are engineering lightweight Generative AI models and implementing sophisticated onboard data compression techniques directly at the edge.</p>
    </div>
    <div class="badge-ongoing">🚀 Ongoing Investigation</div>
  </div>
</div>

<div class="research-row reverse">
  <div class="research-img-container">
    <img src="/assets/dist_ml.webp" alt="Distributed Machine Learning" class="research-img">
  </div>
  
  <div class="research-text">
    <h2 class="research-title">Distributed ML Training & Space-Borne Computation</h2>
    <div class="research-description">
      <p>Scaling models efficiently requires rigorous infrastructure management. Leveraging my experience with multi-GPU lab environments, I am simulating 3D parallel training (Data, Pipeline, and Tensor parallelism) to heavily optimize computational costs and throughput.</p>
      <p>A core aspect of this research involves utilizing internet alongside Wide Area Networks (WAN) to establish better, cheaper data transfer rates. Ultimately, this work is being extended to collaborate on an end-to-end training simulation tailored for futuristic space-borne data centers.</p>
    </div>
    <a href="https://link-to-your-paper.com" target="_blank" class="action-button">
      📄 Read the Publication
    </a>
  </div>
</div>

<div class="research-row">
  <div class="research-img-container">
    <img src="/assets/cv_xai.webp" alt="Computer Vision and XAI" class="research-img">
  </div>
  
  <div class="research-text">
    <h2 class="research-title">Computer Vision & XAI-Based Deepfake Detection</h2>
    <div class="research-description">
      <p>I have developed a novel hand-crafted image descriptor designed to extract highly unique features from input images, significantly improving downstream classification metrics.</p>
      <p>Currently, this descriptor is being applied to fortify Explainable AI (XAI) based deepfake detection systems. By analyzing model behavior against sophisticated white-box and black-box adversarial attacks—including FGSM, BIM, C&W, and PGD—we aim to establish highly robust, interpretable defense mechanisms.</p>
    </div>
    <details class="pub-list">
      <summary>View Associated Publications</summary>
      <ol class="pub-items">
        <li><a href="https://link-to-paper-1.com" target="_blank">Title of Your First Computer Vision Paper (Year)</a></li>
        <li><a href="https://link-to-paper-2.com" target="_blank">Title of Your Second Deepfake Detection Paper (Year)</a></li>
        <li><a href="https://link-to-paper-3.com" target="_blank">Title of Your XAI Adversarial Robustness Paper (Year)</a></li>
      </ol>
    </details>
  </div>
</div>
