# ADR-001: Record architecture decisions

**Date:** 2026-07-18
**Status:** Accepted
**Deciders:** Emanuele (puglieseweb)

## Context

This repository is the documentation home for the pweb-git01 product and is
published to the team's SystemDox Knowledge Base. Decisions about the system
were previously not recorded anywhere durable: context lived in chat threads
and memory, and the published KB had no Design pillar content at all.

The puglieseweb Documentation Standard v1.0 (published as the SystemDox
Documentation Standard) defines how documentation is structured in git:
requirement documents under `docs/requirements/`, architecture decision
records under `docs/design/adr/`, named `ADR-NNN-kebab-title.md`. Its
bootstrap convention is that a new ADR directory starts with this very
document, which doubles as the deterministic marker that the repo
participates in the Design pillar.

## Decision

We record architecture decisions as ADRs in this directory, following the
puglieseweb Documentation Standard v1.0:

- One file per decision, named `ADR-NNN-kebab-title.md`, numbers claimed at
  PR time and never reused.
- Decisions are written in imperative voice, with Context, Decision,
  Consequences and Alternatives Considered sections.
- Accepted ADRs are immutable except status changes and date-stamped
  amendment notes; reversals are new ADRs with bidirectional links.

## Consequences

### Positive

- The KB's Design pillar has a canonical, reviewable home; every decision
  gets a URL the whole organisation can read.
- New contributors and AI agents can reconstruct why the system is the way
  it is without spelunking chat history.

### Negative

- Writing a short ADR becomes part of the definition of done for
  architecturally significant changes — a small, deliberate overhead.

## Alternatives Considered

| Alternative | Why Rejected |
| --- | --- |
| Keep decisions in chat/issues | Not durable, not reviewable, invisible to the KB |
| Wiki pages | Bypass PR review and drift; the standard forbids wikis as canonical stores |

## Related

- puglieseweb Documentation Standard v1.0, §3.2 (Design pillar)
