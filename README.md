<p align="center">
  <img src="https://img.shields.io/badge/version-3.1-blue?style=flat-square" alt="Version"/>
  <img src="https://img.shields.io/badge/license-Proprietary-red?style=flat-square" alt="License"/>
  <img src="https://img.shields.io/badge/claude--code-compatible-green?style=flat-square" alt="Claude Code"/>
  <a href="#support"><img src="https://img.shields.io/badge/sponsor-support%20FORGE-ff69b4?style=flat-square" alt="Support"/></a>
</p>

<p align="center">
  <pre align="center">
███████╗ ██████╗ ██████╗  ██████╗ ███████╗
██╔════╝██╔═══██╗██╔══██╗██╔════╝ ██╔════╝
█████╗  ██║   ██║██████╔╝██║  ███╗█████╗
██╔══╝  ██║   ██║██╔══██╗██║   ██║██╔══╝
██║     ╚██████╔╝██║  ██║╚██████╔╝███████╗
╚═╝      ╚═════╝ ╚═╝  ╚═╝ ╚═════╝ ╚══════╝
  </pre>
</p>

<h3 align="center">Complete Product Companion for Claude Code</h3>
<p align="center"><em>"From idea to production. Every step matters."</em></p>

---

> **⚠️ License Notice:** This software is proprietary. Personal use is permitted. Public forks, redistribution, and commercial use require written permission. See [LICENSE](LICENSE).

---

**FORGE** is a project creation agent for [Claude Code](https://claude.ai/code). It guides you through every step: understanding your idea, researching the market, generating a PRD, making technical decisions, and scaffolding a production-ready project.

---

## Table of Contents

1. [Requirements](#requirements)
2. [Installation](#installation)
3. [How It Works](#how-it-works)
4. [Step-by-Step Walkthrough](#step-by-step-walkthrough)
5. [What FORGE Creates](#what-forge-creates)
6. [Skill Packs](#skill-packs)
7. [FAQ](#faq)
8. [Support](#support)

---

## Requirements

Before installing FORGE, you need:

| Requirement | How to get it |
|-------------|---------------|
| **Claude Code** | Install from [claude.ai/code](https://claude.ai/code) |
| **Node.js 18+** | `curl -fsSL https://bun.sh/install \| bash` (includes Node) |
| **Package manager** | bun (recommended), npm, yarn, or pnpm |

### Optional (but recommended)

| Tool | Purpose |
|------|---------|
| **git** | Version control |
| **gh** | GitHub CLI for repo creation |

---

## Installation

### Option 1: Quick Install (Recommended)

```bash
curl -fsSL https://raw.githubusercontent.com/agentik-os/forge/main/install.sh | bash
```

### Option 2: Manual Install

```bash
# Clone the repository
git clone https://github.com/agentik-os/forge.git
cd forge

# Run the installer
chmod +x install.sh
./install.sh
```

### What the installer does

1. **Detects your environment** - Checks for Claude Code, package managers, existing tools
2. **Creates directories** - `~/.claude/agents/`, `~/.claude/commands/`, `~/.claude/templates/`
3. **Offers optional add-ons** - Choose from agent bundles (Starter, Fullstack, SaaS, Mobile)
4. **Downloads files**:
   - `~/.claude/commands/forge.md` - Main FORGE command
   - `~/.claude/templates/themes/` - Color theme presets
   - Selected agents and commands from catalog

### Verify installation

```bash
claude
# Inside Claude Code, type:
/forge
```

If you see the FORGE banner, you're ready!

---

## How It Works

FORGE follows a 12-step workflow:

```
┌─────────────────────────────────────────────────────────────┐
│                   FORGE v3.1 WORKFLOW                       │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  0. ENVIRONMENT SCAN                                        │
│     → Detects your tools, skills, project folders           │
│                                                             │
│  1. GREETING                                                │
│     → How do you want to start?                             │
│                                                             │
│  2. DISCOVERY                                               │
│     → What are you building? Who for? What problem?         │
│                                                             │
│  3. MARKET RESEARCH (optional)                              │
│     → FORGE searches for competitors, gaps, pricing         │
│                                                             │
│  4. PRD GENERATION                                          │
│     → Creates full Product Requirements Document            │
│     → YOU MUST APPROVE before continuing                    │
│                                                             │
│  5. TECHNICAL DECISIONS                                     │
│     → Framework, styling, backend, auth, payments...        │
│     → EVERY choice is explicit, NOTHING assumed             │
│                                                             │
│  6. DESIGN                                                  │
│     → Theme, colors, dark mode, initial pages               │
│                                                             │
│  7. TOOLING                                                 │
│     → ESLint, Prettier, testing, CI/CD                      │
│                                                             │
│  7.5 SKILL PACKS                                            │
│     → Recommends SEO, Testing, Marketing skills             │
│     → Installs only what you're missing                     │
│                                                             │
│  8. AGENT INTEGRATION                                       │
│     → Sets up Ralph, MANIAC, Sentinel (if installed)        │
│                                                             │
│  9. CONFIRMATION                                            │
│     → Shows full summary, you type 'confirm'                │
│                                                             │
│  10. EXECUTION                                              │
│      → Scaffolds project with latest patterns               │
│                                                             │
│  11. FINAL SUMMARY                                          │
│      → What was created + next steps                        │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## Step-by-Step Walkthrough

### Step 1: Start Claude Code

```bash
claude
```

### Step 2: Launch FORGE

```
/forge
```

You'll see the FORGE banner and an environment analysis:

```
╔══════════════════════════════════════════════════════════════╗
║  🔍 FORGE ENVIRONMENT ANALYSIS                               ║
╚══════════════════════════════════════════════════════════════╝

## 🛠️ TOOLS DETECTED

| Tool | Status |
|------|--------|
| bun | ✅ 1.1.0 (Recommended) |
| npm | ✅ 10.0.0 |
| git | ✅ |

## 📁 PROJECT DIRECTORIES

Found:
- ~/projects/ (5 projects)
- ~/work/ (3 projects)
```

### Step 3: Choose Your Approach

FORGE asks how you want to start:

```
How would you like to start?

1. I have a clear idea - let's discuss it
2. I have a vague idea - help me shape it
3. Let FORGE do the research first
4. I already have a PRD - skip to tech
```

### Step 4: Describe Your Idea

FORGE asks questions to understand your vision:

- **What are you building?** (2-3 sentences)
- **What problem does it solve?**
- **Who is this for?** (B2B, B2C, internal)
- **Do you know any competitors?**

### Step 5: Market Research (Optional)

If you choose research, FORGE searches the web:

```
🔍 FORGE is researching your market...

Searching for:
- Direct competitors
- User complaints (Reddit, reviews)
- Pricing models
- Market gaps

This takes 2-3 minutes...
```

Result: A market research report with competitors, opportunities, and recommendations.

### Step 6: PRD Generation

FORGE generates a complete Product Requirements Document:

```
╔══════════════════════════════════════════════════════════════╗
║  📋 PRODUCT REQUIREMENTS DOCUMENT                            ║
║  [Your Project Name]                                         ║
╚══════════════════════════════════════════════════════════════╝

## 1. EXECUTIVE SUMMARY
## 2. PROBLEM STATEMENT
## 3. TARGET PERSONAS
## 4. FEATURE SPECIFICATION (MVP)
## 5. MONETIZATION STRATEGY
## 6. SUCCESS METRICS
## 7. RISKS & MITIGATIONS
```

**You must approve the PRD before continuing.** FORGE will NOT proceed without your explicit approval.

### Step 7: Technical Decisions

FORGE asks about EVERY technical choice:

| Question | Example Options |
|----------|-----------------|
| Project type | Web, Mobile, Desktop, API, Extension |
| Framework | Next.js, React, Remix, Vue, Svelte |
| Router (if Next.js) | App Router, Pages Router |
| Styling | Tailwind, CSS Modules, Styled Components |
| Components | shadcn/ui, Radix, MUI, Chakra |
| Backend | Convex, Supabase, Firebase, Prisma |
| Auth | Clerk, Better Auth, Auth.js |
| Payments | Stripe, LemonSqueezy, Paddle |
| Project location | ~/projects/, ~/work/, custom |
| Project name | lowercase-with-dashes |
| Port | Auto-suggested based on existing projects |

**Nothing is assumed.** If you want Next.js with App Router, you explicitly choose it.

### Step 8: Design Choices

```
What feeling should your app convey?

1. Professional & Trustworthy
2. Modern & Techy (like Vercel/Linear)
3. Friendly & Approachable
4. Bold & Energetic

Color scheme:
1. Use preset: Minimal Light
2. Use preset: Dark Techy
3. Use preset: Vibrant Purple
4. Paste custom theme (oklch)
```

### Step 9: Skill Packs (NEW in v3.1)

FORGE analyzes your installed skills and recommends packs:

```
╔══════════════════════════════════════════════════════════════╗
║  🎯 SKILL PACKS ANALYSIS                                     ║
║  Recommended for: SaaS Project                               ║
╚══════════════════════════════════════════════════════════════╝

## SEO Pack ⭐ Recommended

| Skill | Status |
|-------|--------|
| seo | ✅ Installed |
| seo-meta | ✅ Installed |
| seo-audit | ❌ Missing |
| schema-markup | ❌ Missing |

Status: 2/6 installed

Would you like to complete this pack?
```

FORGE **never reinstalls** skills you already have.

### Step 10: Confirmation

Before executing, FORGE shows a complete summary:

```
╔══════════════════════════════════════════════════════════════╗
║  📋 PROJECT CONFIGURATION SUMMARY                            ║
╚══════════════════════════════════════════════════════════════╝

## PROJECT
Name: my-saas-app
Location: ~/projects/my-saas-app
Port: 3001

## TECH STACK
Framework: Next.js (App Router)
Styling: Tailwind CSS
Components: shadcn/ui
Backend: Convex
Auth: Clerk
Payments: Stripe

## DESIGN
Theme: Dark Techy
Dark Mode: System preference

## AGENTS
Ralph: ✅ Will configure
MANIAC: ✅ Will configure

Type 'confirm' to proceed.
```

### Step 11: Execution

FORGE creates your project:

```
🔥 Creating your project...

[1/7] Fetching latest docs via Context7...
[2/7] Running create-next-app...
[3/7] Installing dependencies...
[4/7] Setting up shadcn/ui...
[5/7] Creating project structure...
[6/7] Configuring agents...
[7/7] Initializing git...

✅ Done!
```

### Step 12: Next Steps

```
╔══════════════════════════════════════════════════════════════╗
║  🔥 FORGE COMPLETE: my-saas-app                              ║
╚══════════════════════════════════════════════════════════════╝

## NEXT STEPS

1. Configure your API keys:
   Edit .env.local with your Clerk, Convex, and Stripe keys

2. Start the development server:
   cd ~/projects/my-saas-app
   bun run dev

3. Start the backend (in another terminal):
   bunx convex dev

4. Read your PRD:
   cat docs/PRD.md

5. Start building with Ralph:
   /ralph "implement user authentication"
```

---

## What FORGE Creates

### Directory Structure

```
my-project/
├── docs/
│   ├── PRD.md              # Your approved PRD
│   ├── FEATURES.md         # Feature backlog from PRD
│   └── USER-STORIES.md     # Test scenarios for MANIAC
├── src/
│   ├── app/                # Next.js App Router pages
│   ├── components/         # UI components
│   │   ├── ui/             # shadcn/ui components
│   │   └── ...
│   └── lib/                # Utilities
├── convex/                 # Backend functions (if Convex)
├── e2e/                    # Playwright tests
├── .github/
│   └── workflows/          # CI/CD pipelines
├── CLAUDE.md               # AI assistant context
├── @fix_plan.md            # Ralph task list
├── @AGENT.md               # Ralph project context
├── .env.local              # Environment variables (gitignored)
├── .env.example            # Template for team
└── package.json
```

### Documents Generated

| Document | Purpose |
|----------|---------|
| `docs/PRD.md` | Complete product requirements |
| `docs/FEATURES.md` | Prioritized feature backlog |
| `docs/USER-STORIES.md` | Test scenarios for QA |
| `CLAUDE.md` | Context for AI assistants |
| `@fix_plan.md` | Tasks for Ralph autonomous dev |
| `@AGENT.md` | Project context for Ralph |

---

## Skill Packs

FORGE v3.1 includes a Skill Packs system that recommends enhancement modules based on your project type.

### Available Packs

| Pack | Skills Included | Recommended For |
|------|-----------------|-----------------|
| **SEO** | seo, seo-meta, seo-audit, schema-markup, roier-seo, programmatic-seo | Web, Landing, SaaS |
| **Testing** | e2e-testing-patterns, webapp-testing, systematic-debugging, debugging, debugging-strategies | All projects |
| **Design** | web-design-guidelines, shadcn-ui, frontend-design, brainstorming | Web, Landing, SaaS, Mobile |
| **Performance** | vercel-react-best-practices, audit-website | Web, SaaS |
| **Marketing** | page-cro, marketing-ideas, marketing-psychology, launch-strategy, social-content, email-sequence | SaaS, Landing |
| **Convex** | convex, convex-best-practices, convex-realtime | Projects using Convex |
| **Stripe** | stripe-best-practices, pricing-strategy | Projects using Stripe |
| **Mobile** | expo-tailwind-setup, upgrading-expo | Mobile apps |
| **Analytics** | analytics-tracking, data-storytelling | SaaS, Landing |
| **Video** | remotion, remotion-best-practices | Video projects |

### How It Works

1. FORGE scans your installed skills
2. Based on your project type (SaaS, Landing, etc.), it recommends relevant packs
3. Shows what's already installed vs. what's missing
4. You choose which packs to complete
5. Only missing skills are installed - **never reinstalls existing ones**

---

## FAQ

### Q: Do I need to answer every question?

**Yes.** FORGE is designed to be thorough. Every question matters because every technical decision affects your project. This prevents assumptions that lead to rework.

### Q: Can I skip the PRD phase?

**Yes.** If you already have a PRD, choose "I already have a PRD - skip to tech" at the start.

### Q: What if I don't have Ralph/MANIAC installed?

FORGE works without them. It will simply skip the agent integration step. However, having them provides a better development workflow.

### Q: Can I use FORGE for existing projects?

FORGE is designed for new projects. For existing projects, you can run `/forge` and copy relevant parts (like the PRD template or tech decisions) manually.

### Q: How long does the full process take?

Typically 15-30 minutes including market research. The actual scaffolding takes 2-5 minutes.

### Q: Is my data sent anywhere?

FORGE runs entirely within Claude Code. Market research uses web searches but your project details stay local.

---

## Support

If FORGE helps you ship products faster, consider supporting its development.

<p align="center">
  <a href="https://paypal.me/garethsimono">
    <img src="https://img.shields.io/badge/PayPal-Donate-00457C?style=for-the-badge&logo=paypal&logoColor=white" alt="PayPal"/>
  </a>
</p>

<p align="center">
  <sub><strong>PayPal:</strong> simono.gareth@gmail.com</sub>
</p>

<br/>

<table align="center">
  <tr>
    <th>Crypto</th>
    <th>Network</th>
    <th>Address</th>
  </tr>
  <tr>
    <td><strong>USDT</strong></td>
    <td>Arbitrum</td>
    <td><code>0x8709fd7475780d4caa2c6674b06396c57a0530fa</code></td>
  </tr>
  <tr>
    <td><strong>SOL</strong></td>
    <td>Solana</td>
    <td><code>37H9ecXZ2BpWkBEogCcosj6LEBp5uqgBs5fjJgjzNeo7</code></td>
  </tr>
  <tr>
    <td><strong>BTC</strong></td>
    <td>Bitcoin</td>
    <td><code>1CVMhkWDBMt5C5WsE8vmY84KSnFCrgPbZL</code></td>
  </tr>
</table>

<br/>

<p align="center">
  <sub>Your support keeps FORGE maintained and improving. Thank you! 🙏</sub>
</p>

---

## Links

- [Claude Code](https://claude.ai/code) - The AI coding assistant
- [shadcn/ui](https://ui.shadcn.com) - Component library
- [Convex](https://convex.dev) - Backend platform
- [Clerk](https://clerk.com) - Authentication
- [Agentik OS on TAAFT](https://theresanaiforthat.com/@agentik_os/) - More AI tools

---

## License

**Proprietary License** - see [LICENSE](LICENSE)

| Permitted | Not Permitted |
|-----------|---------------|
| ✅ View and study source code | ❌ Public forks or redistribution |
| ✅ Personal, non-commercial use | ❌ Commercial use without permission |
| ✅ Private modifications | ❌ Sublicensing |

**Commercial licensing:** x@agentik-os.com

---

## Credits

- Inspired by **Forge** from X-Men - the mutant inventor who can build anything
- Built for [Claude Code](https://claude.ai/code) by Anthropic
- Created by [Agentik OS](https://github.com/agentik-os)

---

<p align="center">
  <strong>From idea to production. Every step matters.</strong>
</p>
