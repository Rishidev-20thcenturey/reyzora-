<!-- REYZORA portfolio README: project showcase and verified external links. -->

<h1 align="center">REYZORA</h1>

<p align="center">
  <strong>Independent AI research and software projects</strong><br />
  A growing portfolio of experiments, engineering work, and deployed applications.
</p>

---

## Featured project · RAY-IMAGE

<p>
  <strong>RAY-IMAGE</strong> is an independent, experimental text-to-image research project built around a custom VAE, Diffusion Transformers (DiT), flow matching, frozen Qwen3-4B text conditioning, and classifier-free guidance (CFG). The latest project research includes a 110.7M dense DiT v4 baseline and a roughly 482M sparse Mixture-of-Experts DiT v5, with training conducted on free-tier Kaggle T4 GPUs. The repository's main branch currently preserves the older v3 source snapshot; the README distinguishes that source state from the later v4/v5 research record.
</p>

<table>
  <tr>
    <td width="66%" valign="top">
      <a href="https://github.com/Rishidev-20thcenturey/rustes-generative-ai">
        <img
          src="https://raw.githubusercontent.com/Rishidev-20thcenturey/rustes-generative-ai/main/Screenshot_20261023-175533%20%282%29.png"
          alt="Legacy RAY-IMAGE experimental sample grid from an earlier model iteration; not v4 or v5 output"
          width="100%"
        />
      </a>
      <p align="center">
        <sub>Legacy experimental sample gallery from an earlier RAY-IMAGE iteration. These examples are not v4/v5 outputs and are not a controlled benchmark or evidence of current model quality.</sub>
      </p>
    </td>
    <td width="34%" valign="top">
      <h3>Project links</h3>
      <p><strong>Active source code</strong><br />
        <a href="https://github.com/Rishidev-20thcenturey/rustes-generative-ai">Open the RAY-IMAGE repository on main ↗</a>
      </p>
      <p><strong>Technical README</strong><br />
        <a href="https://github.com/Rishidev-20thcenturey/rustes-generative-ai/blob/main/README.md">Current research status, main-branch scope, limitations, and artifacts ↗</a>
      </p>
      <p><strong>Public model repository</strong><br />
        <a href="https://huggingface.co/Rishix500/ray-image-dit-v5-moe">RAY-IMAGE DiT v5 MoE ↗</a>
      </p>
      <p><strong>Public training cache</strong><br />
        <a href="https://huggingface.co/datasets/Rishix500/monet-qwen-cache-200k-v4">MONET + Qwen3-4B cache ↗</a>
      </p>
      <p><strong>Hugging Face profile</strong><br />
        <a href="https://huggingface.co/Rishix500">Rishix500 ↗</a>
      </p>
    </td>
  </tr>
</table>

### At a glance

| Area | Details |
|---|---|
| **Image representation** | VAE v3 at 512 × 512 RGB; 16 latent channels on a 64 × 64 grid |
| **v4 dense baseline** | 110,724,750 parameters; 2D axial RoPE, SwiGLU, and gated text cross-attention; its 120k checkpoint warm-started v5 |
| **v5 sparse MoE** | About 482M total parameters and 204M active per token; 1 shared plus 8 routed SwiGLU experts with top-2 routing |
| **Text conditioning** | Frozen Qwen3-4B; 2,560-dimensional hidden states, truncated to 128 tokens |
| **Training objective** | Flow matching; Euler integration for sampling; optional classifier-free guidance |
| **Compute** | Free-tier Kaggle T4 GPUs |
| **Training status** | v5 logs reach approximately 171.4k steps |
| **Project status** | Experimental research code; no formal image-quality benchmark and not a production image generator |

### Current research state and limitations

The v5 training logs show a modest loss improvement: approximately 1.5 near 127k steps to 1.4 near 170k, with velocity MSE moving from about 1.5 to 1.35. These are training diagnostics, not image-quality measurements.

The v4 samples reviewed so far show more prompt-specific colour and composition than the v5 samples reviewed at 135k steps, but object structure is weak in both. Several v5 samples share similar compositions, and prompt adherence remains uncertain. The 170k v5 checkpoint has not yet been sampled and reviewed. A direct real-prompt versus null-prompt conditioning test and a formal benchmark have not yet been completed.

### Model and artifact access

| Artifact | Current access |
|---|---|
| **DiT v5 MoE main repository** | Public; linked above. The project record reports a 170k checkpoint. |
| **MONET + Qwen cache** | Public; linked above. Its dataset card reports 140,000 samples despite “200k” in the repository name. |
| **DiT v4 dense model and milestones** | Private; not publicly downloadable. |
| **DiT v5 milestones repository** | Private; not publicly downloadable. |
| **VAE v3 512px checkpoint repository** | Private; not publicly downloadable. |
| **Legacy v3 checkpoint** | Private; not publicly downloadable. |

Repository visibility was checked on 6 November 2026. Public repository visibility does not imply that every companion checkpoint, milestone, or dependency is public or independently validated. The main-branch README now includes the latest v4/v5 project research record while clearly stating that v4/v5 source code has not been merged into main.

## Featured project · CraveDirect

<p>
  <strong>CraveDirect</strong> is a deployed food-discovery storefront and full-stack API MVP. It brings restaurant browsing, cuisine filters, menus, cart management, delivery addresses, cash-on-delivery checkout, and order history into one web experience, with a separate read-only directory for discovering restaurants and places.
</p>

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://cravedirect-web.netlify.app/">
        <img src="assets/cravedirect-home.jpg" alt="CraveDirect home page and hero section" width="100%" />
      </a>
      <p align="center"><sub>Storefront</sub></p>
    </td>
    <td width="50%" valign="top">
      <a href="https://cravedirect-web.netlify.app/">
        <img src="assets/cravedirect-discovery.jpg" alt="CraveDirect food discovery search and filters" width="100%" />
      </a>
      <p align="center"><sub>Food discovery</sub></p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <a href="https://cravedirect-web.netlify.app/">
        <img src="assets/cravedirect-restaurants.jpg" alt="CraveDirect restaurant listings and cuisine cards" width="100%" />
      </a>
      <p align="center"><sub>Restaurant listings</sub></p>
    </td>
    <td width="50%" valign="top">
      <a href="https://cravedirect-web.netlify.app/">
        <img src="assets/cravedirect-discovery-footer.jpg" alt="CraveDirect discovery experience and footer" width="100%" />
      </a>
      <p align="center"><sub>Discovery experience</sub></p>
    </td>
  </tr>
</table>

### Project links

- **[Open the live CraveDirect website ↗](https://cravedirect-web.netlify.app/)**
- **[View the source repository ↗](https://github.com/Rishidev-20thcenturey/food-delivery-api)**
- **[Check the live API health endpoint ↗](https://cravedirect-api.onrender.com/api/v1/health)**

### Technology and scope

| Area | Details |
|---|---|
| **Frontend** | React, TypeScript, Vite |
| **Backend** | Node.js, Express 5, typed REST API |
| **Data and API contract** | PostgreSQL, OpenAPI 3.1, automated tests |
| **Hosting** | Netlify storefront, Render API |
| **Current scope** | Restaurant browsing, filters, cart, addresses, cash-on-delivery checkout, order history, and read-only external discovery |
| **Status** | Deployed MVP/demo; not production-hardened |

> **Scope note:** External discovery listings are not automatically orderable through CraveDirect. Online payments and complete worldwide ordering are not implemented.

## Featured project · AI-WIFU

<p>
  <strong>AI-WIFU</strong> is a working full-stack AI companion application centered on expressive anime avatars, character-aware conversation, and live voice interaction. The experience combines animated 2D/3D characters, camera-based vision, generated speech, music, character customization, and browser-side memory in one interface.
</p>

<table>
  <tr>
    <td width="66%" valign="top">
      <a href="https://live-anime-ai-waifu.ai.studio/">
        <img
          src="assets/ai-wifu-lobby.jpg"
          alt="AI-WIFU lobby showing its animated 3D companion, voice-call controls, vision controls, affection level, avatar mode switch, and customization actions"
          width="100%"
        />
      </a>
      <p align="center">
        <sub>Actual AI-WIFU lobby screenshot from the original project repository. Select the image to open the live app.</sub>
      </p>
    </td>
    <td width="34%" valign="top">
      <h3>Project links</h3>
      <p><strong>Live application</strong><br />
        <a href="https://live-anime-ai-waifu.ai.studio/">Open AI-WIFU online ↗</a>
      </p>
      <p><strong>Source code</strong><br />
        <a href="https://github.com/Rishidev-20thcenturey/AI-WIFU-">Open the original AI-WIFU repository ↗</a>
      </p>
      <p><strong>Technical documentation</strong><br />
        <a href="https://github.com/Rishidev-20thcenturey/AI-WIFU-#readme">Features, setup, and architecture ↗</a>
      </p>
    </td>
  </tr>
</table>

### Technology and scope

| Area | Details |
|---|---|
| **Frontend** | React 19, TypeScript, Vite, Tailwind CSS, Motion |
| **Backend and transport** | Node.js, Express, HTTP API routes, WebSocket live-audio bridge |
| **AI integration** | Google Gemini APIs for chat, voice, transcription, vision, and optional music generation |
| **Avatar and interaction** | Three.js, VRM avatar rendering, 2D canvas character, expressions, lip-sync and customization |
| **Personalization** | Character presets, conversation history, affection score, and browser-local memory |
| **Live demo** | [live-anime-ai-waifu.ai.studio](https://live-anime-ai-waifu.ai.studio/) |
| **Status** | Working integrated application; external AI access and browser permissions affect some features |

> **Deployment and privacy note:** The app uses browser storage for some profile, chat, and memory data, and sends selected prompts, images, or audio to the configured AI provider when those features are used. The source README documents remaining deployment-hardening needs, including backend access controls and rate limiting. The live link is provided as an entry point; availability and all provider-dependent features are not independently guaranteed by this portfolio.


---

## More projects

Additional projects will be documented here one at a time, with their own verified screenshots, original repository links, live demos where available, and model or dataset links when applicable.

> **Portfolio scope:** This repository is a project index. The original repositories remain the source of truth for their code and development history; this README does not copy or modify their source files.
