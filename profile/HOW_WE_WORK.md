# How We Work

> A high-level look at our internal development workflow, technology stack, and system architecture.  
> These documents are part of What Comes Next, LLC’s commitment to transparent engineering practices and founder-scale velocity.

---

## 🔧 AI-Augmented Development Workflow

Our technical operations leverage large language models (LLMs) in a structured, repeatable workflow that enables high-quality product development with minimal overhead. This hybrid approach combines strategic architectural insight with tactical execution in the IDE.

### 🧠 Role Breakdown

| Role               | Agent Used           | Description |
|--------------------|----------------------|-------------|
| **Strategist**     | Claude 3 / GPT-4     | Multi-file analysis, architecture refactors, logic debugging |
| **Editor**         | Cursor (VSCode fork) | Context-aware inline edits, function generation, doc updates |
| **Integrator**     | Founder              | Final judgment, testing, deployment, changelog updates |

### 📄 Documentation Stack

- `CHANGELOG.md`: Human-readable task summaries and file change logs
- `CHANGELOG-LLM.md`: LLM-optimized architecture and rationale tracking
- `HOW_WE_WORK.md`: This file — operational methodology and systems documentation
- `SECURITY.md`, `BRANDKIT.md`: Complementary documentation for compliance and consistency

### 🔁 Workflow Steps

1. **Planning**: Claude/GPT is fed changelog context + codebase snippets to suggest refactors or implementations
2. **Drafting**: LLMs generate proposed code or structural changes
3. **Execution**: Cursor is used to edit, refactor, or integrate code directly in the repo
4. **Validation**: The founder tests, validates, and documents all changes
5. **Traceability**: All updates are logged in both human and machine-readable changelogs

This workflow creates a scalable technical system with built-in auditability, offline compatibility, and documentation clarity—while preserving founder-level control of all production logic.

---

## 🛠️ Tech Stack Overview

We use modular, privacy-first tools designed to support secure, high-velocity product development with no third-party telemetry or platform lock-in.

### 📦 Core Technologies

- **Frontend**:  
  - Next.js (App Router)  
  - React (13+)  
  - TailwindCSS (custom brand config)

- **Backend**:  
  - Supabase (Postgres, Auth, Storage)  
  - Self-hosted Node APIs (for Cron, Mailer, Admin Ops)

- **DevOps / Infra**:  
  - Docker + local testing environments  
  - ProtonVPN + Cloudflare Tunnel (for remote access and webhook security)  
  - Shell-based CI/CD workflows (no cloud CI)  
  - Local LLM infrastructure (GPU-enabled servers running LLaMA variants)

- **LLM System**:  
  - Claude 3 and GPT-4 used for planning and architecture  
  - Cursor.dev for inline code assistance  
  - CHANGELOG-based knowledge transmission between agents

- **Security & Privacy**:  
  - No external analytics or telemetry  
  - Environment-aware routing and hardened API entrypoints  
  - Encryption at rest and in transit (Postgres, backups, mailer services)

---

## 📁 File Locations

This file lives in: .github/HOW_WE_WORK.md

It is intended to be read alongside:
- `.github/SECURITY.md`
- `.github/BRANDKIT.md`
- `.github/profile/README.md`

For contributions, refer to the public documentation in `wcn-thecatalyst`.

---

