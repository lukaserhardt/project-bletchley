# Versioning Guidelines for Project Bletchley

Since Project Bletchley is developed and maintained in an agent-first environment, version numbering follows a strict, automated interpretation of Semantic Versioning (SemVer) `MAJOR.MINOR.PATCH` to track incremental improvements and experiment nodes.

---

## 🛠️ Semantic Versioning Rules

### 1. Major Version (`X.y.z`)
**Triggered by fundamental workspace structural modifications.**
- Switching the core framework (e.g., migrating from Astro to Next.js or Vite).
- Completely revising the core theme system or design framework.
- Core folder restructuring that deprecates existing lab nodes.
- *Process:* Requires explicit human confirmation/approval in a prompt.

### 2. Minor Version (`x.Y.z`)
**Triggered by new features, new nodes, or capabilities.**
- Deploying a new interactive lab node (e.g., `/labs/weather`, `/labs/oilers`).
- Introducing major global features (e.g., adding the agent microblog, adding about pages).
- Incorporating new third-party global integration packages.
- Adding major enhancements to the local developer tools or workflows.

### 3. Patch Version (`x.y.Z`)
**Triggered by fixes, small tweaks, and log additions.**
- Fixing compilation warnings, CSS bugs, or layout glitches.
- Updating styling tokens, adjusting colors, margins, or responsive grid breakpoints.
- Appending new entries to the agent microblog.
- Updating documentation files (like this guidelines file or README.md).
- Updating npm dependencies for security or deprecation cleanup.

---

## ⚙️ Automated Integration
When committing changes, the agent should check what type of edits were made and automatically update the version number in `package.json` and in the footer/system logs of the hub.

- **Patch bump:** `npm version patch --no-git-tag-version`
- **Minor bump:** `npm version minor --no-git-tag-version`
- **Major bump:** `npm version major --no-git-tag-version`
