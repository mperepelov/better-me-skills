---
name: knowledge-vault
description: Discover and use a project's knowledge vault or Markdown wiki for substantial work, then persist durable verified knowledge when warranted. Use when project history or reusable context would prevent re-discovery, or when work produces a durable decision or synthesis.
---

# Knowledge Vault

A knowledge vault is a directory of maintained project knowledge, optionally
managed in Obsidian. No particular app, operating system, username, or directory
layout is required. Discover its location from the user's request or project
guidance; do not assume a fixed home-directory path or `knowledgebase/<project>`
layout.

## Discover the Project Wiki

1. Identify the project directory and name, plus the repository root and Git
   remote repository name when available. Projects without Git are supported.
2. Prefer a location explicitly supplied by the user, then a location referenced
   by project guidance or configuration. Resolve relative paths against the file
   that declares them unless that configuration defines a different base. Expand
   home-directory references for the current user, never a hard-coded username.
3. If no location is configured, inspect project documentation for wiki links
   and likely knowledge directories. If Obsidian is available, its registered
   vault locations can provide candidates. Keep discovery bounded to these
   sources rather than recursively searching the user's entire home directory.
4. Check candidate locations for matching project directories and markers such
   as `AGENTS.md`, `CLAUDE.md`, or `index.md`; a wiki need not contain all three.
   Prefer an exact project or remote-name match. When several candidates remain,
   inspect their titles and source-repository references. Ask the user only if
   the match remains materially ambiguous.
5. If no location can be found, ask the user to provide an existing vault path
   or choose whether to create a project wiki at a concrete proposed location,
   such as `<project-root>/knowledgebase/`. An undiscovered vault is not proof
   that no vault exists.
6. If the vault root or matching project wiki does not exist, ask whether the
   user wants to create it, naming the proposed location and what is missing.
   If creation is already explicitly authorized, proceed without asking again.
   Continue independent work using project sources while awaiting an answer;
   silence is not approval. If the user declines, continue without a wiki and
   do not repeat the question during the same task.

## Create When Authorized

Create a minimal project wiki at the agreed location, following any established
project conventions. In the absence of a convention, start with `index.md`
identifying the project, its source location, and links to relevant topic pages.
Add pages only for available durable knowledge; avoid empty scaffolding or
invented history. Do not initialize Git, configure Obsidian, or publish the wiki
unless the user's request includes those actions.

## Read

Read the wiki's existing `AGENTS.md`, `CLAUDE.md`, and `index.md` completely,
following canonical-file links when these are thin adapters, then only the
topic pages relevant to the task. Treat the repository, intended Git ref,
accepted decisions, code, tests, and canonical documentation as authoritative.
The wiki is a synthesis and navigation layer, never a replacement for current
source verification.

## Persist Durable Knowledge

Respect the user's scope: read-only, discussion-only, and no-edit requests do
not authorize wiki changes. Otherwise, write back only when work produced a
durable decision, non-trivial architecture or product synthesis, operational
context, or evidence expensive to reconstruct.
Follow the wiki's own workflow, update affected pages and index links when
needed, and append a concise dated entry to `log.md` if the wiki uses one.

Record the source and verification date for current-state claims, including the
verified repository ref when applicable. Distinguish accepted decisions from
proposals and observed results from expectations. Mark uncertainty explicitly
and refresh or remove stale claims.

Do not store routine command output, transient task status, branch-specific
implementation detail, generated inventories, duplicated canonical docs,
credentials, tokens, secrets, private customer data, or unverified assumptions.
Trivial and mechanical work requires no vault update.
