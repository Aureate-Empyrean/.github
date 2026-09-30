# Aureate Empyrean

**Open software. Private by design.**

Aureate Empyrean is an open-source, self-hosted software ecosystem built around a simple principle:

> **Your data should belong to you.**

Instead of putting your digital life behind mandatory cloud accounts, subscriptions, and disconnected services, Aureate Empyrean is building focused applications that can work together while remaining independently understandable and useful.

Run it on infrastructure you control. Keep ownership of your data. Connect only what you choose.

## The Ecosystem

### Empyrean Nexus
**The control plane of Aureate Empyrean.**

Nexus connects independent Aureate Empyrean applications through shared infrastructure for authentication, permissions, resource references, events, storage, lifecycle management, backup and interoperability.

It coordinates the ecosystem without becoming the owner of each application's domain data.

### Meridian
**People, organizations, relationships and the knowledge around them.**

A structured personal knowledge system for people and organizations — relationships, interactions, facts, claims, sources, life events, stories and accumulated context.

### Mnemosyne
**Notes, knowledge and personal organization.**

A workspace for notes, tasks, projects, collections and connected knowledge, designed around everyday workflows rather than database administration.

### Atlas
**Your personal geographic layer.**

Places, areas, routes and eventually visits and location history — built around geographic information you own, with external discovery remaining explicit.

### Hermes
**Communication, unified on your terms.**

Messages, conversations, calls and email across multiple sources, preserving both original source data and a useful normalized communication model.

### Chronos
**Time, calendars and events.**

The ecosystem's operational layer for calendars, events, dates, recurrence and time-based workflows.

### Argus
**Personal captured media.**

Photos and other personally captured or imported media, with metadata, organization and future recognition capabilities.

### Lyra
**Your multimedia library.**

A personal library for music and, over time, movies, television, books and audiobooks — with Aureate-native workflows instead of a collection of wrapped third-party applications.

### Janus
**A secure local-first vault.**

Credentials, identities, recovery material, secure notes and other sensitive information, designed around explicit custody and strong separation from ordinary ecosystem data.

### Astra
**Contextual intelligence across Aureate Empyrean.**

A shared intelligence layer that can assist inside supported applications without becoming another copy of your data.

Applications decide what context and tools Astra receives. Intelligence providers are replaceable, and local models are first-class.

> **Tools belong to Aureate Empyrean. Intelligence is replaceable.**

## How it fits together

Aureate Empyrean is not one enormous application and not a bundle of unrelated services.

Each application owns its domain. Empyrean Nexus provides the common substrate that lets them cooperate without collapsing their data models into one database.

Cross-application relationships use stable resource identities and explicit references. Applications can project or cache information from another domain when useful, but the original owner remains authoritative.

The result is one ecosystem without requiring one application to know everything.

## Principles

- **Open source**
- **Self-hosted**
- **Privacy by design**
- **Local-first where practical**
- **User-owned and portable data**
- **Explicit permissions and integrations**
- **Interoperable without shared domain ownership**
- **Local knowledge before external discovery**
- **No artificial paywalls**
- **No data harvesting**
- **No mandatory cloud dependency**

## Development

Aureate Empyrean is in active early development.

The architecture is being defined before individual applications are allowed to drift into incompatible assumptions. Shared contracts, ownership boundaries and architectural decisions live in the [`architecture`](https://github.com/Aureate-Empyrean/architecture) repository.

Empyrean Nexus is the first shared infrastructure implementation. Domain applications are developed independently on top of those contracts.

---

> **Not a system that knows everything about you.  
> A system that knows what you know.**

Aureate Empyrean does not need to observe your life to be useful. It should remember, connect and work with what you deliberately choose to give it.
