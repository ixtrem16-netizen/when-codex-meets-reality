# When Codex Meets Reality

### Real-world experiments with Codex, persistent agents, infrastructure, devices and physical systems

> **I rarely start technical projects by writing code anymore.**
>
> **I talk.**

I'm **David Gagné**, an IT technician and team lead working in an MSP environment in Quebec, Canada.

I have always been passionate about technology.

But ChatGPT and Codex fundamentally changed the way I interact with it.

Many of my projects now begin with a voice conversation in French from my phone.

I describe what I want to accomplish.

ChatGPT helps me transform that intent into a structured technical objective.

I then hand that objective to Codex, often through a persistent project environment I built called **Codex Hub**.

From there, the agent can investigate, build, test and interact with real systems.

My role remains to provide context, define constraints, authorize consequential actions, observe reality and decide whether the result is actually correct.

My workflow increasingly looks like this:

**Voice → ChatGPT → Structured Goal → Codex → Tools → Real System → Evidence → Human Judgment**

The implementation technology keeps changing.

The human interface increasingly does not.

---

# Why this repository exists

I originally thought of Codex as a coding agent.

Then I started giving it more tools.

First development environments.

Then files and shells.

Then SSH.

Then virtual machines.

Then Android through ADB.

Then networking and infrastructure.

Then persistent agent environments.

Then fabrication workflows.

Then external platforms.

Eventually I realized that I was no longer only experimenting with a coding assistant.

I was exploring a much broader question:

> **What happens when an increasingly capable reasoning system is given tools and asked to interact with reality?**

This repository documents selected experiments from that journey.

It is not intended to prove that every experiment was autonomous or that every outcome constitutes a formal benchmark.

It is a record of real-world human-agent collaboration and the questions that emerged from it.

---

# My working method

My professional background strongly influences how I work with AI.

I generally follow a loop similar to:

**Need → Context → Hypothesis → Action → Observation → Adjustment → Validation → Documentation**

I care about the distinction between:

**a command that completed successfully**

and

**a real-world objective that was actually satisfied.**

Depending on the project, validation may involve:

- logs
- automated tests
- file comparison
- SHA-256 hashes
- health checks
- virtual machines
- reboots
- rollback testing
- physical hardware
- measurements
- screenshots
- or direct human observation

A disappearing error is not automatically proof of recovery.

A successful build is not automatically a working deployment.

A virtual boot is not automatically physical qualification.

A confident model response is not evidence that an assumption is true.

---

# Professional IT work

Codex is not limited to my personal laboratory.

I also use AI as part of real technical investigation and automation work.

## Backup and recovery troubleshooting

In one documented Datto troubleshooting case following a Debian migration, the investigation progressed through several layers:

- kernel/module state
- DKMS
- local snapshots
- service behavior
- debugger analysis
- library behavior
- backup execution
- incremental backup
- Screenshot Verification

One of the most useful lessons from this case was simple:

> **Making the original crash disappear did not prove that the backup system worked.**

The investigation continued until backup behavior could be validated at a more meaningful operational level.

---

## Proxmox and storage troubleshooting

I have used AI-assisted investigation for infrastructure problems where storage was unavailable during a Proxmox installation.

The work involved reasoning across:

- RAID controllers
- kernel behavior
- drivers
- firmware
- IOMMU
- boot parameters
- installation behavior
- post-install validation

The system eventually became usable, while the working workaround remained explicitly separated from a definitive proof of root cause.

That distinction matters to me.

---

## Targeted Windows application recovery

In another case, a Windows business application was crashing during an important workflow.

Crash-dump analysis with Codex helped narrow the failure to a .NET JIT optimization path.

Rather than globally changing Windows behavior, a targeted launcher was prepared to modify the runtime behavior only for the affected process.

The immediate workflow became usable again.

The result was documented as a **workaround**, not falsely presented as a permanent vendor fix.

---

## Automation and endpoint management

My AI-assisted work also includes:

- PowerShell
- Windows SYSTEM-context automation
- RMM workflows
- software deployment
- post-install configuration
- network configuration
- validation scripts
- troubleshooting procedures
- documentation and handoffs

I frequently use ChatGPT to turn observations — sometimes dictated verbally — into structured technical tasks, documentation, escalation notes and procedures.

---

# Codex Hub — persistent agents

As my Codex usage increased, individual terminal sessions became an organizational problem.

I wanted persistent project-oriented agent sessions that I could access from different devices, especially my phone.

That led to **Codex Hub**.

Codex Hub became a way to organize work around projects and sub-projects while keeping long-running Codex environments hosted elsewhere in my infrastructure.

One audited state contained:

> **161 Codex conversations mapped to 161 unique working directories**

The phone becomes the human interface.

The agent and project environment remain persistent elsewhere.

This created new questions that have little to do with code generation:

- How should persistent agent projects be separated?
- Where should project state live?
- How should secrets be handled?
- How should one agent hand work to another?
- How do you resume a project after days or weeks?
- What information belongs in conversation context versus external documentation?

---

# Maison Docs — external operational memory

Long-running projects made me realize that conversation history alone was not enough.

I worked with AI to develop **Maison Docs**, a structured private operational knowledge system.

Its purpose is not simply to store notes.

Documentation is designed so that another technician — or a future Codex instance with no previous conversational context — can understand:

- what the system does
- how components relate
- what has been verified
- what remains unknown
- how to diagnose problems
- what actions are allowed
- how to validate a result
- how to roll back
- where to escalate

This became an experiment in **external memory for persistent agents**.

---

# Maison Vault, Identity and agent boundaries

As agent access increased, secret handling and authorization became increasingly important.

My environment evolved to separate:

- operational documentation
- authentication
- secrets
- agent execution
- management tooling

I use separate systems and explicit boundaries rather than treating a `.env` file or a prompt as a security architecture.

One principle became especially important:

> **Technical capability is not the same thing as authorization.**

An agent may technically have broad access in a controlled laboratory environment.

The human-requested task still defines the authorized scope.

---

# Maison RMM

I also worked with AI on a private remote-management environment for systems in my personal/family infrastructure.

The project includes concepts such as:

- inventory
- policies
- remote tasks
- remote terminal workflows
- sessions
- MFA
- CSRF protection
- revocation
- agent updates
- rollback behavior

I do not present experimental systems as perfectly secure.

Known weaknesses remain part of the documentation until they are actually resolved and revalidated.

That is another principle I try to preserve when working with agents:

> **Documentation should describe reality, not the state we wish existed.**

---

# MediSAM — long-horizon engineering

One of my largest Codex projects is **MediSAM**, a recovery and diagnostic platform involving:

- Windows
- Linux
- WinPE
- WIM images
- virtual machines
- physical boot media
- deployment infrastructure
- build systems
- release management
- rollback
- recovery
- documentation
- physical qualification

Codex participates in source work, scripting, builds, troubleshooting, dependency verification, deployment, testing and handoff documentation.

A particularly important state in the project looked like this:

```text
BUILD VERIFIED    = YES
QEMU VERIFIED     = YES
PHYSICAL VERIFIED = NO
