# AuraGuard: The End-to-End Digital Trust Platform
**Team Cipher | InnovateHER 2026**
*Developed by: Manya E A, Chinmayi Mohan, and Varshitha S*

---

## 1. Executive Summary
**AuraGuard** is a state-of-the-art proactive defense and compliance platform designed to protect individual digital likeness and privacy against unauthorized AI scraping, face-swapping, and deepfake generation. Using deep adversarial learning and automated legal tools, AuraGuard provides a dual-layer defense:

1. **Proactive Face Inoculation (StealthCloak)**: Injecting imperceptible mathematical gradients into images that scramble facial embeddings in latent space, rendering them useless for AI model training or scraping.
2. **Reactive Legal Enforcement (LexiBot)**: Generating statutory legal takedown notices under the Indian Information Technology Act (IT Act) 2000 and the Digital Millennium Copyright Act (DMCA) to mandate rapid removals from hosting platforms.

---

## 2. Platform Architecture & Features

### 🛡️ Tab 1: StealthCloak (Proactive Likeness Immunity)
* **Adversarial Perturbation (FGSM/PGD)**: Computes subtle gradient perturbations targeting the face region's 512-dimensional embeddings via a pretrained `InceptionResnetV1` (vggface2). It decouples the mathematical identity vectors from the visual image.
* **3-Column Real-time Visualizer**:
  * **Original Portrait (Vulnerable)**: Displays the clean, uploaded input photo.
  * **Scattered Pixels (Perturbation Map)**: Displays the normalized absolute pixel difference $|Cloaked\_Face - Original\_Face|$ colormapped using `magma` to highlight coordinates of maximum landmark disruption.
  * **Cloaked Portrait (Protected)**: Displays the final inoculated image where subtle noise is smoothly blended using a feathered Gaussian blur mask (SSIM > 98% visually identical to humans).
* **EXIF Metadata Privacy Scrubber**: Automatically strips location, device, and GPS metadata upon generation (0 KB privacy footprint).
* **LSB Steganographic Provenance Certificate**: Embeds an invisible, cryptographically signed payload containing timestamp and SHA-256 integrity hash for authenticity verification.
* **Robustness Integrity Stress-Test**: Simulates lossy social media compression (JPEG quality 60) to verify that adversarial vectors survive transmission over WhatsApp, Instagram, and other channels.

### ⚖️ Tab 2: LexiBot (Automated Statutory Dispatch)
* **Incident Intake Form**: Dynamically parses the hosting platform, violator handle, infringing URL, date, and description.
* **Statutory Citations**: References **Section 66E** (violation of privacy) and **Section 67A** (obscenity/morphed media) of the **Indian IT Act, 2000** alongside **Section 512(c)** of the **DMCA**.
* **Integrity Token System**: Computes a unique SHA-256 Ref ID signature for the notice, ensuring records are tamper-proof.
* **Direct Redressal Channels**: Direct integration links and emails for the National Cyber Crime Portal and major intermediary grievance officers.

---

## 3. Technology Stack

* **Front-End / UI**: Streamlit web application running on a premium Black & Emerald Green Cyber Onyx theme with customized glassmorphism styling.
* **Face Bounding Box Detection**: `MTCNN` (Multi-task Cascaded Convolutional Networks) for precise facial landmark extraction.
* **Facial Representation Network**: `InceptionResnetV1` evaluating facial vector similarity.
* **Optimization & Math**: PyTorch for backpropagation of loss gradients (maximizing cosine distance); `scikit-image` for Structural Similarity Index (SSIM) visual fidelity score.
* **Image Processing**: OpenCV and Pillow (PIL) for image composites, difference computations, and LSB manipulation.

---

## 4. Key Metrics & Defensive Targets

| Metric | Target | Description |
| :--- | :--- | :--- |
| **Human Visual Fidelity (SSIM %)** | **> 98%** | Measures structural similarity of the cloaked face crop compared to the original. Visual difference is imperceptible to humans. |
| **AI Identity Match Confidence** | **< 20%** | Measures Cosine Similarity between face embeddings of original and cloaked portraits. Lower values denote identity decoupling in AI models. |
| **Scrambling Defense Index** | **> 80%** | The inverse of similarity, demonstrating the platform's ability to scramble landmark coordinates. |
