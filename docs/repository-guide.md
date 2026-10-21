# Repository guide

## Responsibilities

| Repository | Owns |
| --- | --- |
| `.github` | Public organization profile and shared contributor resources |
| `Lightstream-Engine` | Reusable s&box runtime systems, editor extensions, and authoring tools |
| `Projekt-Alpha` | The s&box project, game code, scenes, and project-specific documentation |
| `bazzite-cosmic` | The Bazzite-derived operating-system experiment; preserve upstream attribution and licensing |

Keep development tools such as przm.DEV in their own source repository when they are published. Do not put tool application code in this organization-profile repository, or link to a repository that does not yet exist.

Use the current repository names in clone URLs, documentation, and integrations. A rename should be a separate change with updates to dependent links and local tooling.

## Documentation structure

Start every project with a concise README containing its purpose, current implementation status, prerequisites, setup steps, verification steps, and source map. Keep detailed setup and architecture notes under `docs/` when needed.

Document a feature as implemented only when its source or a verified release supports that description. Lightstream-Engine now targets s&box; its standalone Swift prototype is preserved on separate branches. Describe the current main branch as a foundation until executable SDK code and a verified integration exist.

Use repository Issues for active tasks and decisions that need ownership. Keep historical checklists clearly marked as reference material.

## Suggested issue workflow

A small shared project board can use **Backlog → Ready → In progress → Review → Done**. Define each Issue with a problem, a bounded outcome, and acceptance criteria. Assign it when someone takes ownership; link the implementation pull request.

Keep labels modest: `bug`, `enhancement`, `documentation`, and `task` are enough to begin. Add area or priority labels only when they help actual triage. The shared forms intentionally do not require labels to exist.

## Maintainer settings to apply separately

These are recommendations, not settings changed by this documentation pull request.

| Repository | Suggested About description | Suggested topics |
| --- | --- | --- |
| `.github` | Studio Prism's organization profile and shared contributor resources. | `studio-prism`, `documentation` |
| `Lightstream-Engine` | Studio Prism's framework and SDK work built in and around s&box. | `sbox`, `csharp`, `gamedev`, `sdk` |
| `Projekt-Alpha` | Studio Prism's experimental s&box game prototype. | `sbox`, `csharp`, `gamedev`, `prototype` |
| `bazzite-cosmic` | Studio Prism's experimental COSMIC-focused Bazzite fork. | `bazzite`, `cosmic-desktop`, `linux`, `experiment` |

Pin Lightstream-Engine and Projekt-Alpha as the primary public projects. Add bazzite-cosmic if operating-system research is part of the intended public presentation. Keep public pins limited to work a visitor can understand from its README.

Review organization bio, avatar, website, and contact links for current ownership before changing them. Use the approved Prism emblem consistently; avoid adding an unverified domain or contact address.

Review branch rules separately. For a small team, make review and build requirements match the checks and reviewers that actually exist. Do not enable a required check before it has a reliable workflow, or create rules that leave the team unable to merge.

Do not alter repository visibility, archived state, names, or licensing as incidental cleanup. Keep archived projects preserved; assess active experimental repositories with their maintainers before reclassifying them.
