# AbbVie Discovery Luxury

Luxurious, 3D-interactive concept website inspired by AbbVie's AI-driven drug discovery (ARCH platform, generative AI, target identification, etc.).

**Features:**
- Premium dark navy (#071D49) luxury aesthetic
- Interactive 3D molecular / particle scenes (React Three Fiber)
- Fancy smooth animations (Framer Motion)
- AbbVie logo as favicon and branding
- Local development + Cloudflare Pages ready

## Best Prompt for Codex

Copy the prompt below into Codex (ChatGPT Codex, Cursor Composer, or similar coding agent) to generate the full website.

---

**PROMPT START**

You are an elite frontend engineer and 3D web artist specializing in luxury digital experiences for biopharma. Build a complete, production-ready Next.js 15 application (App Router, TypeScript, Tailwind CSS v4 or latest) for a luxurious interactive website celebrating AbbVie's AI-powered drug discovery.

**Core Requirements:**

1. **Branding & Theme**
   - Primary color: #071D49 (AbbVie navy). Secondary luxury accents: soft champagne gold (#D4AF37 or #C9A961), platinum, crisp white.
   - Typography: Elegant modern sans (Inter or similar via next/font) with refined tracking.
   - Logo: Use the provided public/abbvie-logo.svg (lowercase wordmark approximation) in the navbar and as favicon. Generate favicon.ico / apple-touch-icon from it. Replace with official assets if available later.
   - Overall feel: Ultra-premium, sophisticated, cinematic – think luxury watch + high-end science lab + Apple product site. Dark mode primary, subtle light sections if needed.

2. **3D & Animations (make this the star)**
   - Use @react-three/fiber, @react-three/drei, three.
   - Hero: Full-viewport interactive 3D scene – floating molecular structures, DNA helix, or glowing particle clouds representing compounds. User can orbit, zoom, and interact. Soft lighting, reflections, luxury materials (glass, metal).
   - Additional 3D elements: Scroll-linked camera, floating cards with 3D tilt, interactive molecule explorer section where users can manipulate a sample protein/compound model.
   - Animations: Framer Motion for page transitions, stagger reveals, magnetic buttons, smooth scroll. Luxurious timing (slow, elegant ease). Optional GSAP for complex sequences.
   - Cursor glow, subtle particle trails, glassmorphism panels.

3. **Content Structure (pages/sections)**
   - **Hero**: Bold headline "Accelerating Breakthroughs" or "AI at the Heart of Discovery". Subtitle about ARCH platform and bringing medicines to patients faster. Dual CTAs. 3D background.
   - **Innovation**: Sections on AI target finding, generative design, data convergence. Luxury cards with hover 3D effects.
   - **Interactive Explorer**: Dedicated 3D canvas where users explore a sample molecule or data visualization.
   - **Impact**: Animated stats (90+ compounds, $13B+ R&D, 75 conditions, etc. inspired by real AbbVie numbers).
   - **Process / Stories**: Horizontal or scroll storytelling of the discovery journey.
   - Footer with elegant links.

4. **Technical**
   - Fully responsive. On mobile, simplify 3D or use lighter alternatives for performance.
   - Optimized images, lazy loading, code splitting.
   - SEO: Proper meta, Open Graph with AbbVie branding.
   - Accessibility: Keyboard nav, reduced motion support.
   - Clean component architecture: components/Hero.tsx, components/MoleculeScene.tsx, components/Navbar.tsx, etc.
   - Include package.json with all deps, next.config.ts (compatible with Cloudflare), tailwind.config, app/layout.tsx, app/page.tsx.
   - Environment ready for Cloudflare Pages (static export or OpenNext adapter if needed; prefer simple static + edge where possible).

5. **Deliverables**
   - Complete working codebase that runs with `npm install && npm run dev`.
   - README.md with local setup, build, and Cloudflare Pages deployment steps (e.g. connect GitHub repo or `npx wrangler pages deploy`).
   - No placeholders – make the visuals and copy impressive and complete.
   - Ensure `npm run build` succeeds.

Generate all files. Make it visually stunning, interactive, and luxurious. Prioritize the 3D experience and polished animations above all else.

**PROMPT END**

---

## Local Setup (after Codex generates the code)

```bash
git clone https://github.com/ramkarthik77/abbvie-discovery-luxury.git
cd abbvie-discovery-luxury
npm install
npm run dev
```

## Deploy to Cloudflare Pages

1. Push the generated code to this repo (or a new one).
2. In Cloudflare Dashboard → Workers & Pages → Create → Pages → Connect to Git.
3. Select this repository.
4. Build command: `npm run build`
5. Build output directory: `.next` or `out` (depending on next.config – Codex should set `output: 'export'` for static if desired).
6. Or use Wrangler: `npx wrangler pages deploy .next` after build.

For full Next.js features on Cloudflare, consider the OpenNext Cloudflare adapter.

## Notes

- This is a concept/demo site inspired by public information about AbbVie's real AI and R&D work (ARCH platform, generative AI, etc.).
- Replace the logo SVG with official AbbVie assets before any public use.
- Primary brand color confirmed as #071D49.

Enjoy the luxury experience.
