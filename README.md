AuraGuard: An End-to-End Proactive Data Poisoning and Automated Digital Trust Platform
<img width="1848" height="88" alt="image" src="https://github.com/user-attachments/assets/d30dbaac-b310-49d3-9fcb-ebc1aa742348" />


# 🛡️ AuraGuard: Proactive Deepfake Defense & Biometric Inoculation Platform

**AuraGuard** is an active defense framework designed to protect biometric facial identity against unauthorized AI deepfake cloning, facial manipulation models, and malicious facial recognition scrapers. 

Instead of relying purely on passive post-hoc detection, AuraGuard applies **imperceptible adversarial noise (immunization cloaks)** to images before publication. To human eyes, the image remains visually identical; however, generative models and AI scrapers encounter complete latent representation collapse.

---

## 🌟 Key Features

* **Proactive Biometric Inoculation (StealthCloak):** Embeds bounded adversarial perturbations ($\ell_\infty \le 8/255$) that disrupt latent feature maps in models like FaceNet, InsightFace, and diffusion-based swap generators.
* **Standardized IQA Evaluation Protocol:** Integrates pure PyTorch Image Quality Assessment metrics to mathematically verify visual imperceptibility versus defensive strength.
* **Latent Disruption Telemetry:** Real-time cosine similarity and facial landmark drift evaluation to quantify protection effectiveness.
* **Regulatory Compliance & Risk Assistant (LexiBot):** Interactive legal and trust advisor mapping biometric security postures to EU AI Act and GDPR synthetic identity frameworks.

---

## 🔬 Mathematical Image Quality & Defense Verification

To confirm that defensive perturbations do not degrade visual aesthetics, AuraGuard evaluates inoculated images across four standard benchmarks:

| Metric | Target / Benchmark | Description |
| :--- | :--- | :--- |
| **SSIM (Structural Similarity)** | **$> 0.96$** | Preserves core structural details, luminescence, and contrast. |
| **PSNR (Peak Signal-to-Noise)** | **$> 38\text{ dB}$** | Guarantees high visual fidelity with near-zero human perceivable distortion. |
| **Perceptual Distance (LPIPS)** | **$< 0.05$** | Deep feature perceptual difference remains negligible. |
| **AI Scraper Match (Cosine)** | **$< 0.20$** | Biometric embeddings are scrambled, preventing AI identity verification. |


[ Raw Face Input ]
│
▼
[ Defensive Perturbation Engine ] ─── (Bounded Gradient Inoculation)
│
├────────────────────────────────┬────────────────────────────────┐
▼                                ▼                                ▼
[ Inoculated Image ]           [ IQA Verification ]          [ Scraper Vulnerability Test ]
(Human Imperceptible)         (PSNR, SSIM, LPIPS)              (Latent Cosine < 0.20)
## 🏗️ Technical Architecture
