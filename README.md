# Tone Skills Plugin (`tone-skills`)

A curated collection of engineering tone and communication skills for AI coding assistants (Google Antigravity, GitHub Copilot, VS Code, Claude Code, and Roo Code). 

This plugin equips AI assistants with authentic developer voices tailored for different engineering contexts—from hands-on mentor evaluations to formal enterprise RFC specifications.

---

## 🎭 Skill Catalog

| Skill Name                         | Tone Persona                          | Primary Use Case                                                         | Output Style                                                                                |
|:-----------------------------------|:--------------------------------------|:-------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| **`srinivas-tone`**                | **Srinivas Rao Tammireddy**           | Mentor updates, technical evaluations, spikes, bug investigation reports | Grounded in local testing, bottom-line first, exact metrics, real-time troubleshooting flow |
| **`formal-technical-tone`**        | **Enterprise Architect / Governance** | Client-facing RFCs, architecture whitepapers, executive decision memos   | Authoritative third-person, risk matrices, compliance tables, phased rollouts               |
| **`pragmatic-peer-tone`**          | **Senior Peer Developer**             | Team chat, PR descriptions, peer code reviews, Slack discussions         | Plain conversational verbs, direct cause-and-effect, unpretentious                          |
| **`technical-documentation-tone`** | **Staff / Systems Engineering Team**  | Internal engineering wikis, Confluence ADRs, spike documentation         | 13-dimension comparative matrices, deep-dive trade-offs, Mermaid flowcharts                 |

---

## 📁 Repository Structure

```text
tone-skills/
├── plugin.json                           # Antigravity Plugin manifest
├── README.md                             # Plugin documentation & install guide
├── AGENTS.md                             # Universal agent instructions & author profile
├── rules/
│   └── developer-interaction-rules.md    # Developer interaction rules & coding guidelines
├── skills/
│   ├── srinivas-tone/                    # Hands-on consultant tone
│   │   └── SKILL.md
│   ├── formal-technical-tone/            # Enterprise RFC tone
│   │   └── SKILL.md
│   ├── pragmatic-peer-tone/              # Peer developer tone
│   │   └── SKILL.md
│   └── technical-documentation-tone/     # Internal technical docs tone
│       └── SKILL.md
└── .agents/
    ├── skills.json                       # Registers skills/ for workspace discovery
    └── rules/
        └── developer-interaction-rules.md
```

---

## 🚀 Installation & Usage

### 1. Universal One-Line Install (`npx skills add`) — *Recommended*

The easiest and most flexible way to install these skills into any project (supporting Antigravity, Claude Code, Cursor, Windsurf, Roo Code, and Cline):

#### Install All Skills from GitHub:
```bash
npx skills add srinu2003/tone-skills
```

#### If Your Repo is Private (via SSH):
```bash
npx skills add git@github.com:srinu2003/tone-skills.git
```

#### Install a Specific Skill Only:
```bash
npx skills add srinu2003/tone-skills --skill srinivas-tone
npx skills add srinu2003/tone-skills --skill formal-technical-tone
```

#### Target a Specific AI Agent:
```bash
npx skills add srinu2003/tone-skills --agent claude-code
npx skills add srinu2003/tone-skills --agent cursor
```

---

### 2. Google Antigravity Plugin Methods

#### Option A: Workspace / Project-Level (Recommended for Teams)
In any target project (e.g., `custom-lwc`), add this repository as a submodule:
```bash
git submodule add https://github.com/srinu2003/tone-skills.git .agents/plugins/tone-skills
```
Antigravity automatically detects `.agents/plugins/tone-skills` and makes all skills available immediately.

#### Option B: Local Linking via `plugins.json` (Zero-Copy)
If you have `tone-skills` cloned locally, you can link it directly in another project's `.agents/plugins.json`:
```json
{
  "entries": [
    { "path": "c:/Users/tsiri/Projects/tone-skills" }
  ]
}
```

#### Option C: Global Installation (Machine-Wide)
To make these skills available across **every project** on your machine without configuring each workspace:
```bash
git clone https://github.com/srinu2003/tone-skills.git ~/.gemini/config/plugins/tone-skills
```

---

### 3. VS Code (GitHub Copilot, Claude Code, Roo Code, Cline)

* **GitHub Copilot**: Copilot automatically reads `AGENTS.md` at the root of the repository to adopt your developer profile, testing guidelines, and legacy code preservation rules.
* **Claude Code / Roo Code / Cline**: These extensions natively support the **Open Agent Skills standard** (`skills/<name>/SKILL.md`). You can invoke skills directly via slash commands:
  - `/srinivas-tone`
  - `/formal-technical-tone`
  - `/pragmatic-peer-tone`
  - `/technical-documentation-tone`

---

## 👤 Author Profile

- **Developer**: Srinivas Rao Tammireddy
- **Core Principles**:
  1. Direct, bottom-line-first communication.
  2. Grounded in actual scratch org and local test verification.
  3. Strict preservation of commented legacy code and production workarounds.
  4. Exact adherence to platform limits (Locker Service, CSP, 5.0 MB Static Resource quotas).

---

## 📄 License

MIT License. Free for personal and commercial use.
