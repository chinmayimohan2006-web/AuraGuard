# AuraGuard: The End-to-End Digital Trust Platform
**Team Cipher**
*Developed by: Chinmayi Mohan, Manya E A, and Varshitha S*

---

## 1. Executive Summary
**AuraGuard** is a state-of-the-art proactive defense and compliance platform designed to protect individual digital likeness and privacy against unauthorized AI scraping, face-swapping, and deepfake generation. Using deep adversarial learning and automated legal tools, AuraGuard provides a dual-layer defense:

1. **Proactive Face Inoculation (StealthCloak)**: Injecting imperceptible mathematical gradients into images that scramble facial embeddings in latent space, rendering them useless for AI model training or scraping.
2. **Reactive Legal Enforcement (LexiBot)**: Generating statutory legal takedown notices under the Information Technology Act (IT Act) 2000 and the Digital Millennium Copyright Act (DMCA) to mandate rapid removals from hosting platforms.

---

## 2. Platform Architecture & Features

### 🛡️ Tab 1: StealthCloak (Dual-Engine Proactive Likeness Immunity)
* **Dual-Engine Core**:
  * **Engine 1: Biometric Landmark Scrambling**: Computes subtle gradient perturbations targeting the face region's 512-dimensional embeddings via a pretrained `InceptionResnetV1` (vggface2). It decouples the mathematical identity vectors from the visual image.
  * **Engine 2: Latent Diffusion Defense**: Computes perturbations targeting high-dimensional encoder representations using a surrogate intermediate feature model, making the image resilient against latent diffusion editing and inpainting.
* **3-Panel Visual Display**:
  * **Panel 1: Original Clean Portrait**: Displays the clean, uploaded input photo marked as vulnerable to scraping.
  * **Panel 2: Forensic Perturbation Map**: Displays the normalized absolute pixel difference $|Cloaked\_Face - Original\_Face|$ colormapped using `magma` with adaptive magnification to highlight coordinates of maximum landmark disruption.
  * **Panel 3: Inoculated Output**: Displays the final protected image (SSIM > 97% visually identical to humans).
* **EXIF Metadata Privacy Scrubber**: Automatically strips location, device, and GPS metadata upon generation.
* **LSB Steganographic Provenance Certificate**: Embeds an invisible, cryptographically signed payload containing timestamp and SHA-256 integrity hash for authenticity verification.
* **Forensic Analysis & Social Media Stress-Test**:
  * **Robustness Integrity Stress-Test**: Simulates lossy social media compression (Instagram/WhatsApp JPEG quality=60 downsampling) to test protection survivability, rendering post-compression SSIM, match confidence, and latent disruption rates.

### ⚖️ Tab 2: LexiBot (Automated Statutory Dispatch)
* **Incident Intake Form**: Parses platform, violator handle, infringing URL, date, and description.
* **Statutory Citations**: Cites **Section 66E** and **Section 67A** of the **Indian IT Act, 2000** and **Section 512(c)** of the **DMCA**.
* **Integrity Token System**: Computes a unique SHA-256 Ref ID notice signature.
* **Direct Redressal Channels**: Direct integration links and emails for the National Cyber Crime Portal and major intermediary grievance officers.

---

## 3. Technology Stack

* **Front-End / UI**: Streamlit web application running on a premium Black & Emerald Green Cyber Onyx theme with customized glassmorphism styling.
* **Face Bounding Box Detection**: `MTCNN` (Multi-task Cascaded Convolutional Networks) for precise facial landmark extraction.
* **Facial Representation Network**: `InceptionResnetV1` evaluating facial vector similarity.
* **Optimization & Math**: PyTorch for backpropagation of loss gradients; `scikit-image` for Structural Similarity Index (SSIM) visual fidelity score.
* **Image Processing**: OpenCV and Pillow (PIL) for image composites, difference computations, and LSB manipulation.

---

## 4. Key Metrics & Defensive Targets

| Metric | Target | Description |
| :--- | :--- | :--- |
| **Human Visual Fidelity (SSIM %)** | **> 97%** | Measures structural similarity of the cloaked face crop compared to the original. Visual difference is imperceptible to humans. |
| **Biometric Identity Match** | **< 20%** | Measures Cosine Similarity between face embeddings of original and cloaked portraits. Lower values denote identity decoupling in AI models. |
| **Latent Diffusion Immunity Rate** | **> 85%** | Measures latent space representation disruption to prevent inpainting and deepfake manipulation. |
