# Aureate Empyrean

**Open software. Private by design.**

Aureate Empyrean is an open-source, self-hosted ecosystem of interoperable personal software. Each application owns one part of your digital life — people, notes, time, places, photos, media, communication, secrets — and they cooperate through shared contracts instead of a shared database.

> **Your data should belong to you.**

There are no mandatory cloud accounts, no subscriptions around core functionality and no telemetry. You run it on infrastructure you control, you keep the data in documented, exportable formats, and you decide what connects to what.

Aureate Empyrean does not observe your life. It remembers what you choose to give it.

## Applications

Maturity is stated per application. *Implemented* means working code with automated tests; it does not mean finished or security-audited. The authoritative, dated record is the [implementation status](https://github.com/Aureate-Empyrean/architecture/blob/main/implementation-status.md).

### Implemented

| Application | Purpose | Maturity | Source |
|---|---|---|---|
| **Empyrean Nexus** | The control plane: authentication, permissions, resource references, events, storage, lifecycle, backup and interoperability. Coordinates the applications without owning their domain data. | Implemented and tested. Pre-release, not security-audited. | [empyrean-nexus](https://github.com/Aureate-Empyrean/empyrean-nexus) |
| **Mnemosyne** | Notes, tasks, projects and collections, designed around everyday workflows. | Implemented and tested. | [mnemosyne](https://github.com/Aureate-Empyrean/mnemosyne) |
| **Chronos** | Calendars, events, dates and recurrence. Can read dated items that other applications choose to share. | Implemented and tested. | Repository not yet public |
| **Meridian** | People, organizations and relationships, with interactions, life events and the context around them. | Implemented and tested. Some planned areas are not built. | Repository not yet public |
| **Atlas** | Your personal geographic layer: places, a map, categories and markers. | Early implementation. Areas, routes and collections are not built. | [atlas](https://github.com/Aureate-Empyrean/atlas) |
| **Argus** | Personally captured photos and media, with bulk import, library backups and optional local face recognition. | Implemented and tested. Recognition is off until you enable it. | [argus](https://github.com/Aureate-Empyrean/argus) |
| **Lyra** | A personal media library. Films and series are implemented; music and books are planned. | Partially implemented. | [lyra](https://github.com/Aureate-Empyrean/lyra) |

### In development

| Application | Purpose | Maturity | Source |
|---|---|---|---|
| **Janus** | A local-first encrypted vault for credentials, identities and other sensitive records, independent of Nexus. | Development build. The cryptographic design has not been independently reviewed; it must not hold real secrets yet. | Repository not yet public |
| **Enceladus** | Training, strength and progress tracking. | Not yet an ecosystem module. An existing prototype is the starting point and has known blockers to resolve before integration. | Not yet published |

### Planned

| Application | Purpose | Maturity |
|---|---|---|
| **Hermes** | Unified communication history: messages, conversations, calls and email from many sources. | Designed, not implemented. |
| **Documents** | Document creation and editing as a module, so Nexus never becomes an editor. | Scope not finalized; the name is a working title. |

### Astra — a planned shared capability

Astra is the intended contextual intelligence layer of the ecosystem. It is **not a deployed application** and not a domain module: it owns no data of its own.

The design: applications decide what context and tools Astra receives, local models are first-class, providers are replaceable, and the AI proposes while you commit. Nothing in the ecosystem depends on it.

> **Tools belong to Aureate Empyrean. Intelligence is replaceable.**

## How it fits together

Each application owns its domain. Nexus provides the common substrate — identity, permissions, references, events, backup — that lets them cooperate without collapsing their data models into one database.

- **Ownership follows domains.** Applications never read each other's databases. They use documented APIs, events and references.
- **References, not copies.** Cross-application links point to stable resource identities. When something is unavailable, a link degrades to an unresolved reference instead of silently breaking.
- **Nexus stays small.** It provides infrastructure and does not learn domain concepts.
- **Modules stay independently understandable** while participating in one ecosystem.

## Principles

- Open source and self-hosted first
- User-owned, exportable and portable data
- Local-first where practical; local knowledge before external discovery
- Explicit permissions and integrations; installed is not trusted
- Manual, inspectable updates, each preceded by a verified backup
- No artificial paywalls, no data harvesting, no mandatory cloud dependency

## Development status

Aureate Empyrean is in active early development, built by an independent developer. It is not a finished product, and some components are pre-release or unreviewed for security. Treat anything labelled development or planned accordingly, and keep backups.

Architecture is defined before applications are allowed to drift into incompatible assumptions. Not every repository is public yet; applications marked as such will be linked when they are.

## For contributors and developers

Start with the [architecture repository](https://github.com/Aureate-Empyrean/architecture). It holds no application code and is the canonical source for:

- [Principles](https://github.com/Aureate-Empyrean/architecture/blob/main/principles.md) and the [ecosystem architecture](https://github.com/Aureate-Empyrean/architecture/blob/main/architecture.md)
- One [specification per module](https://github.com/Aureate-Empyrean/architecture/tree/main/modules), including what is decided, planned and still open
- [Architecture decision records](https://github.com/Aureate-Empyrean/architecture/blob/main/decisions/README.md)
- The [current implementation status](https://github.com/Aureate-Empyrean/architecture/blob/main/implementation-status.md)

Read the relevant module specification before changing any repository, and use each repository's Issues for module work.

---

> **Not a system that knows everything about you.  
> A system that knows what you know.**
