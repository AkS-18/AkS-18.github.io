# Prompt Log & Refinement History

**Student:** Akash Sangeeth  
**Activity:** Personal Portfolio Blog Generation & Refinement  
**Target:** Live GitHub Pages Site (`https://AkS-18.github.io`)  

---

## 1. Initial Generation Prompt (Step 2)

```text
Act as a senior front-end engineer and UI/UX designer. Build a complete, responsive, one-page personal portfolio blog for Akash Sangeeth, a 2nd-year (Semester 3) Computer Science & Engineering student. 

Requirements:
1. Tone & Style: Sleek, high-contrast dark mode aesthetic (inspired by modern developer tools like Linear and GitHub Dark) using deep charcoal/slate backgrounds (#0c0d10, #111318), crisp typography with Inter and JetBrains Mono, subtle glowing accents, and smooth transitions.
2. Structure & Sections:
   - Header/Navigation: Logo (<Akash Sangeeth/>), links to About, Skills, Projects, Milestones, Contact, and direct GitHub button.
   - Hero Section: Professional introduction, badge showing "Semester 3 · Computer Science & Engineering", call-to-action buttons ("Explore Projects", "Get in Touch", "GitHub Profile"), and key metric cards.
   - About Section: Academic overview, engineering philosophy, and cards summarizing hands-on practices.
   - Skills Section: Grouped category cards for Programming Languages, Web & AI, Blockchain & Security, Version Control, Developer Tools, and Problem Solving.
   - Projects Section: Must include both Hackathon innovations (BookByBlock and WeatherGPT) and curriculum artifacts (Activities 1–4) with repository links.
   - Experience / Milestones: Timeline of B.Tech CSE education and practical engineering achievements.
   - Contact Section: Clean contact card with email (akashsangeeth2007@gmail.com), LinkedIn (https://www.linkedin.com/in/akash-sangeeth/), and GitHub (https://github.com/AkS-18).
3. Specific Projects & Links to Include:
   - BookByBlock: Blockchain-powered ticketing platform using NFT tickets and dynamic QR codes to eliminate fraud and unauthorized resale.
   - WeatherGPT: AI-powered climate platform with personalized weather insights, interactive maps, and what-if simulations.
   - Activity 1: Hello World — VS Code Setup (https://github.com/AkS-18/PB_Activity1)
   - Activity 2: Git & GitHub Remote Setup (https://github.com/AkS-18/PB-Activity-2)
   - Activity 3: GitLens & Live Share Collaboration (https://github.com/AkS-18/PB-R25EF018-Activity3)
   - Activity 4: LeetCode Solutions Repository (https://github.com/AkS-18/leetcode-solutions)
4. Technical constraint: Generate this as a clean, self-contained single-page file that can be previewed immediately in any browser by double-clicking index.html and uploaded straight to GitHub Pages without requiring complex build steps or node server dependencies.
```

---

## 2. Follow-Up Refinement Prompts (Step 4)

### Refinement Prompt 1: Project Categorization & Hackathon Highlighting
* **Prompt:**
  ```text
  "The projects section currently displays all six items in a single flat list. Can you add interactive filter tabs (All Works, Hackathons, Curriculum Labs) so visitors can quickly isolate my hackathon work from my course activities? Also, visually accentuate the two hackathon cards (BookByBlock and WeatherGPT) with a glowing featured border and a distinctive green 'Hackathon Project' badge."
  ```
* **What Changed (Before / After):**
  * *Before:* All projects were shown uniformly in a 6-item grid without categorization.
  * *After:* Added an interactive JavaScript tab filter allowing users to switch between "All Works (6)", "🚀 Hackathon Innovations (2)", and "📚 Curriculum Labs (4)", while styling BookByBlock and WeatherGPT with prominent emerald badges and gradient borders.

### Refinement Prompt 2: Single-File Standalone Execution & Direct GitHub Pages Compatibility
* **Prompt:**
  ```text
  "When opening the project file locally or uploading to GitHub Pages, the page fails to launch because the initial version relied on Vite bundling and external module scripts (<script type='module' src='/src/main.tsx'>). Please provide a fully self-contained index.html file with embedded CSS and vanilla JavaScript that launches instantly when double-clicked and can be uploaded directly to GitHub via the web interface without any terminal build steps."
  ```
* **What Changed (Before / After):**
  * *Before:* Opening `index.html` directly in a browser produced a blank white screen due to CORS module loading errors and missing Node.js dev server execution.
  * *After:* Generated a zero-dependency, self-contained `index.html` at the project root containing all styles, SVG vector icons, interactive filtering scripts, and full responsiveness that launches immediately in any web browser and can be committed directly to GitHub Pages.

### Refinement Prompt 3: Expanded Technical Skill Taxonomy
* **Prompt:**
  ```text
  "In the technical skills section, expand beyond generic labels to reflect both my core coursework and my hackathon tech stacks. Include Solidity, Smart Contracts, Dynamic QR Codes, and OpenAI/LLM APIs alongside Python, Java, Git, and LeetCode."
  ```
* **What Changed (Before / After):**
  * *Before:* The skills section only listed basic programming and tools (Python, Java, Git, VS Code).
  * *After:* Categorized technical skills into 6 distinct cards covering Programming Languages, AI & Web Platforms, Blockchain & Decentralization, Version Control & Git, Developer Workflows, and Computer Science Core.

### Refinement Prompt 4: Academic Details, Contact Deduplication & Hero Animation
* **Prompt:**
  ```text
  "Please make these specific refinements:
  1. Let's Connect & Collaborate: Remove duplicate email and LinkedIn buttons so there is only one button for each, retaining GitHub and existing styling.
  2. Education & Training: Update university to REVA University and start year to 2025 (not 2024).
  3. Practical Developer Sequence: Update timeline from 2024-2025 to '2026 – Present'.
  4. Hero Name Animation: Add a smooth sequential letter-by-letter reveal animation to 'Akash Sangeeth' on initial load.
  5. Hero Subtitle: Update 'CSE Student' to 'Computer Science and Engineering Student'."
  ```
* **What Changed (Before / After):**
  * *Before:* Contact section had duplicate icon and text buttons for email and LinkedIn; education listed 2024 start without university name; developer sequence showed 2024–2025; hero heading was static; subtitle was abbreviated "CSE Student".
  * *After:* Removed duplicate contact buttons; explicitly added REVA University with 2025 start; set Practical Developer Sequence to 2026 – Present; added a modern CSS letter-reveal animation for "Akash Sangeeth" with accessibility labels; updated tagline to full "Computer Science and Engineering Student".

### Refinement Prompt 5: Hero Hierarchy Fix, Name Correction & Hackathon Card Cleanup
* **Prompt:**
  ```text
  "Three specific corrections:
  1. The hero section shows the 'Semester 3 · Computer Science & Engineering' pill above the name, making the name feel secondary. Reorder so 'Akash Sangeeth' appears first as the dominant heading, the semester pill below it, then the professional subtitle.
  2. The hero name currently displays as 'Akash S' — change it to the full name 'Akash Sangeeth'. Keep the existing letter-by-letter animation.
  3. Remove the 'View on GitHub' buttons from the BookByBlock and WeatherGPT hackathon cards, as there are no public repositories for these projects."
  ```
* **What Changed (Before / After):**
  * *Before:* Hero showed the semester pill above the name, making 'Akash S' appear secondary; hackathon cards had broken GitHub links pointing to the profile root.
  * *After:* Hero now leads with the full name 'Akash Sangeeth' as the primary visual element, followed by the semester pill and subtitle. The letter-by-letter animation was preserved and extended to cover the full 14-character name. 'View on GitHub' buttons removed from both hackathon cards.

### Refinement Prompt 6: Premium Typography Upgrade & Navbar Rebrand
* **Prompt:**
  ```text
  "Two typography refinements only — do not change layout, content, colors, or animations:
  1. Hero name font: Replace the generic Inter bold with a more refined, premium display typeface. Desired character: modern editorial grotesk, strong display personality, professional developer portfolio aesthetic. Not futuristic or decorative. The letter-by-letter reveal animation must be preserved exactly.
  2. Navbar top-left branding: Remove the < and /> code bracket symbols entirely. It should read simply 'Akash Sangeeth' as a personal wordmark. Give it a cleaner, more refined font with better letter spacing — not a monospace developer logo style."
  ```
* **What Changed (Before / After):**
  * *Before:* Hero name used generic Inter ExtraBold 800; navbar logo displayed `< Akash Sangeeth />` in JetBrains Mono, looking like a code snippet rather than a personal brand.
  * *After:* Hero name now uses Bricolage Grotesque (variable editorial grotesk from Google Fonts) at ExtraBold 800 with the animation fully preserved. Navbar wordmark changed to Plus Jakarta Sans at 600 weight with 0.02em letter-spacing and a subtle hover opacity effect. Code brackets removed completely.

