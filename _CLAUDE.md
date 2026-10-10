---
obsidian-second-brain: true
vault_path: /Users/alvin/Documents/Obsidian Vault
platform: hermes

# Vault Configuration for Obsidian Second Brain

## Identity
name: Alvin
role: Creator, Designer, Developer
primary_email: alvin.b.koech@gmail.com

## Vault Structure
# Folder mapping for entity resolution (Phase 2 reconcile in nightly)
folders:
  entities: People
  concepts: Knowledge
  decisions: Decisions
  projects: Projects
  areas: Areas
  daily: Daily
  inbox: Inbox
  research: Research
  logs: Logs
  reviews: Reviews

## External Integrations
# Are.na
arena_username: astrocrn
arena_channels:
  - Strand
  - EXCI
  - Modus Operandi
  - Ideas many many ideas
  - AETREA
  - Rieko
  - Phisome

# Notion
notion_workspace: Cortex
notion_databases:
  - Projects
  - Tasks
  - Areas
  - School
  - Personal
  - Finance
  - Health
  - ART
  - MUSIC
  - SPACE
  - SOCIAL

## AI-First Rules (non-negotiable)
# Every note written by skills MUST follow these rules:
ai_first:
  preamble: true  # Every note starts with "## For future agent"
  frontmatter: true  # Rich frontmatter with type, date, tags, etc.
  wikilinks: true  # Use [[wikilinks]] for all references
  recency_markers: true  # External claims carry (as of YYYY-MM, source)
  source_preservation: true  # Source URLs preserved verbatim
  confidence_levels: true  # Mark confidence: stated | high | medium | speculation

## Sync Configuration
# External sync settings
sync:
  arena_folder: ARENA
  notion_api: configured  # Already set up in Hermes
  auto_neaten: false  # Contents unchanged, only punctuation/grammar
  cross_reference: true  # Maintain blockid ↔ notion-id ↔ vault-path links

## Scheduled Agents
# All times in UTC+3 (EAT)
cron:
  morning: "0 8 * * *"  # 8:00 AM daily
  nightly: "0 22 * * *"  # 10:00 PM daily
  weekly: "0 18 * * 5"  # 6:00 PM Fridays
  health_check: "0 21 * * 0"  # 9:00 PM Sundays
  external_sync: "0 10 * * 1"  # 10:00 AM Mondays

## Project Mapping (Phisome Synchrony Layer)
# How external sources map to vault locations
mapping:
  # Are.na Channels → Vault Folders
  "ARENA/Strand": "Projects/Strand"
  "ARENA/EXCI": "Projects/EXCI"
  "ARENA/Modus Operandi": "Areas/Modus Operandi"
  "ARENA/Ideas many many ideas": "Inbox"
  "ARENA/AETREA": "Projects/AETREA"
  "ARENA/Rieko": "Projects/Rieko"
  "ARENA/Phisome": "Projects/Phisome"
  
  # Notion Databases → Vault Folders
  "Cortex/Projects": "Projects"
  "Cortex/Areas": "Areas"
  "Cortex/School": "School"
  "Cortex/Personal": "Personal"
  "Cortex/ART": "Creative/ART"
  "Cortex/MUSIC": "Creative/MUSIC"
  "Cortex/SPACE": "Creative/SPACE"
  "Cortex/Finance": "Admin/Finance"
  "Cortex/Health": "Admin/Health"

## Tags Taxonomy
tags:
  types:
    - type/person
    - type/project
    - type/area
    - type/decision
    - type/task
    - type/idea
    - type/concept
    - type/meeting
    - type/resource
  
  status:
    - status/active
    - status/incubating
    - status/stalled
    - status/done
    - status/archived
  
  priority:
    - priority/critical
    - priority/high
    - priority/medium
    - priority/low
  
  source:
    - source/arena
    - source/notion
    - source/vault
    - source/web
    - source/x
    - source/youtube

---

## For future agent

This is the master configuration file for Alvin's Obsidian Second Brain. All skills and cron jobs reference this file for vault structure, identity, and integration settings.

**Key principles:**
- The vault is the source of truth for all knowledge
- Are.na = canonical text surface (public/thinking)
- Notion = operational layer (tasks, timelines, shares)
- Obsidian = local working surface + mirror (everything as plain files)
- All sync is additive: never delete, only add/update/link
- AI-first formatting: every note optimized for future agent retrieval

**When processing:**
1. Always read this file first to understand the vault structure
2. Follow the AI-first rules strictly
3. Maintain cross-references between Are.na, Notion, and vault
4. Log all operations to Logs/ folder
5. Never modify existing content destructively
