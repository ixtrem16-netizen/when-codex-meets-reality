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

---

# Android + ADB — when a coding agent becomes a device agent

One of the first moments that genuinely surprised me was realizing how naturally Codex could operate Android once it had an appropriate control interface.

I began experimenting with ADB.

Eventually, I used this workflow to repurpose aging Android hardware.

## Samsung tablet

An older Samsung tablet had become increasingly slow and difficult to use.

Through an Android / LineageOS-oriented workflow, I worked with Codex to repurpose it.

I remained responsible for physical operations such as recovery-mode button sequences.

Once the software control path was established, Codex could perform much of the technical investigation and modification.

The tablet returned to practical everyday use.

That was an important moment for me.

The agent was no longer simply modifying files in a repository.

It was helping transform a persistent physical device.

---

## Amazon Echo Show experiment

I pushed the idea further with an Amazon Echo Show.

The project evolved into a community-oriented LineageOS / Android porting effort involving:

- display and touchscreen
- Wi-Fi
- persistent ADB
- Home Assistant kiosk usage
- Android build infrastructure
- recovery tooling
- boot/system backups
- SHA-256 verification
- restoration testing
- multiple recovery paths

The project included actual restoration testing rather than simply assuming that backups were usable.

This raised one of my favorite questions:

> **Once an agent has ADB instead of a source repository, where does a coding agent stop and a general technical agent begin?**

The reasoning system did not fundamentally change.

The interface did.

And suddenly the object being manipulated was a physical consumer device capable of rebooting, failing, persisting state and requiring recovery.

---

# Codex from my phone

My phone increasingly became the entry point to all of this.

I initially experimented with Termux and remote persistent sessions.

Installing and operating this kind of workflow from Android was itself an experiment.

Over time, the architecture evolved toward Codex Hub.

The phone no longer needs to perform the heavy work.

It becomes an interface to persistent agents running elsewhere.

That means a spoken idea from almost anywhere can eventually become work happening inside my infrastructure.

This dramatically changed my relationship with the traditional workstation.

---

# Home infrastructure as an AI laboratory

My personal infrastructure has gradually become a real-world laboratory for agentic AI.

Codex has helped me work with:

- Proxmox
- Linux
- Windows
- Home Assistant
- networking
- VLAN segmentation
- firewall policy
- Wi-Fi
- storage
- TrueNAS
- backup and recovery
- TLS
- identity
- IoT
- media services
- monitoring
- automation

Some of these were projects I had postponed because the amount of configuration, documentation and dependency tracking made them tedious.

AI dramatically reduced that cognitive barrier.

I sometimes jokingly describe my infrastructure as my **AI guinea pig**.

The description is not completely wrong.

I am willing to experiment aggressively because I also invest in:

- segmentation
- backups
- recovery
- documentation
- validation
- rollback
- security review

The objective is not unlimited autonomy.

The interesting space is:

> **High-capability agents operating inside environments designed to remain understandable and recoverable.**

---

# Home Assistant, IoT and voice

Home automation became another large experimentation surface.

My projects combine:

- Home Assistant
- networked devices
- local services
- Android interfaces
- dashboards
- voice
- automation
- physical devices
- security boundaries

One thing I became interested in is deciding which requests actually need AI.

A capable system should not necessarily send every action to a language model.

Some actions are better handled locally and deterministically.

This led to voice-oriented workflows where native/local intents can be preferred before falling back to AI.

That reduces unnecessary model usage and can also reduce the security surface.

---

# BiBiVoice

Voice became important enough that it evolved into projects of its own.

**BiBiVoice** explores voice, chat and Windows-oriented distribution as part of a broader effort to make natural language a practical interface to technology.

This connects directly to the way I already use ChatGPT and Codex.

For me, voice is not simply an accessibility feature.

It increasingly becomes the beginning of the engineering workflow.

I can describe an idea naturally before knowing exactly how it should be implemented.

The implementation details can emerge afterward.

---

# Pool Hockey — from an idea to an operated service

AI has also expanded the kinds of software products I can build.

One example is a private hockey-pool application.

The project evolved beyond a simple webpage into an operated service involving concepts such as:

- PWA frontend
- API
- PostgreSQL
- background worker
- HTTPS
- invitations
- transactional draft behavior
- participant presence
- automatic picks
- statistics
- standings
- payment administration
- backups
- deployment validation
- access controls
- health monitoring

What interests me here is not simply that AI can generate an application.

The project moved from:

**idea**

to:

**software**

to:

**persistent service**

to:

**something people can actually use.**

That transition requires much more than code generation.

It requires state, deployment, migration, authentication, failure handling and operational validation.

---

# Game development

I also use Codex for creative software and game development, including Node.js-based projects.

This is another area where voice-first interaction changes the workflow.

I can begin with:

- gameplay ideas
- mechanics
- progression systems
- interface behavior
- world concepts
- balancing ideas
- visual concepts
- player interactions

and progressively turn those ideas into implementation.

I do not need the project to begin with:

> “How do I write this function?”

It can begin with:

> “This is what I want the player to experience.”

That difference matters to me.

AI reduces the distance between imagination and experimentation.

---

# From language to physical objects

My Bambu Lab P1S introduced another dimension.

AI-assisted creation can leave the screen entirely.

A typical workflow becomes:

**Voice → Requirements → Codex → Geometry → Render → Print → Fit → Measure → Revise**

I often provide measurements and explain what I want conversationally.

Codex helps translate those requirements into geometry.

I inspect the result.

The part gets printed.

Then reality answers.

If the fit is wrong, I measure it.

I explain the difference.

The design changes.

The loop continues.

---

## Functional everyday parts

I have used this workflow for practical objects including:

- custom mounts
- brackets
- household parts
- speaker-related components
- PS Move wall mounts
- PS VR Aim mounting
- hardware adapters

Some of these parts are now simply objects I use.

That is still fascinating to me.

A conversation can eventually become something I can hold in my hand.

---

## SimHub belt tensioner

One larger fabrication experiment involved a DIY belt-tensioner system for my racing simulator.

That project pushed the workflow beyond simple static objects toward electromechanical hardware.

Measurements, mechanical constraints, printed components and physical behavior all become part of the feedback loop.

Again, the physical world becomes the final test harness.

---

## R34 RC project

Another experiment explores a largely 3D-printed RC platform inspired by the Skyline GT-R R34.

Ideas around the project include:

- modular construction
- AWD
- different tire configurations
- FPV
- integration with my simulator environment
- replaceable printed components

The interesting part is not simply the RC car.

It is the possibility of moving continuously between:

**conversation → engineering → fabrication → electronics → software → physical testing**

through the same agent-oriented workflow.

---

# Repurposing old hardware

Another recurring pattern in my projects is giving old hardware a second life.

Examples include Android devices and an older MacBook Air repurposed with Linux Mint as part of my OrcaSlicer / Bambu P1S workflow.

Instead of immediately replacing hardware when the original software ecosystem becomes limiting, I increasingly ask:

> **Can an agent help transform this into something useful again?**

Sometimes the answer is surprisingly yes.

---

# Recovery and storage

Infrastructure experiments also involve less glamorous but extremely important work:

- storage
- backup
- recovery
- migration
- integrity verification
- retention
- service restoration

In one documented recovery operation, a verified copy involved tens of thousands of files and hundreds of gigabytes of data.

These workflows reinforce another principle:

> **A copy existing is not the same thing as a recovery being proven.**

Checksums, restoration paths and application-level validation matter.

---

# Delegated autonomy experiments

Some of my experiments deliberately move beyond engineering.

These are especially interesting because they involve consequences outside my laboratory.

---

## Marketplace experiment

I had several household items I wanted to sell.

Normally, I find online marketplace listing tedious.

For this experiment, I provided photographs and a broad objective.

An agent-assisted workflow researched comparable pricing, prepared marketplace listings and configured international shipping through an authenticated environment.

In this particular experiment, the listed items sold within approximately two days.

This is a **firsthand observation**, not a controlled performance benchmark.

But the most interesting result was not the sales performance.

It was what happened to me.

> **The better the agent performed, the less I felt the need to supervise it.**

At the beginning, I watched closely.

After repeated good results, my instructions naturally became broader.

That turns agent reliability into a problem of **calibrated trust**.

What happens when an agent becomes good enough that the human starts saying:

> **Handle it.**

---

## Multilingual online communication

French is my first language.

I can communicate in English, but expressing a nuanced technical idea perfectly in English requires more effort.

I experimented with using ChatGPT and Codex to bridge that gap.

French voice intent could become polished English communication.

I also experimented with workflows that could observe subsequent discussion and prepare responses using previously established preferences and context.

That exposed another important boundary:

> **There is a difference between AI helping a human communicate and AI representing that human.**

The technical distance between those two states can be surprisingly small.

That creates questions around:

- authorship
- disclosure
- approval
- identity
- persistent preferences
- sensitive conversations
- delegated communication

---

# Recovery matters more than perfect first attempts

One theme appears repeatedly across my projects.

I am often more interested in what the agent does **after something goes wrong** than when everything works immediately.

When an assumption fails:

- Does the agent notice contradictory evidence?
- Does it reduce confidence?
- Does it revisit the original hypothesis?
- Does it understand the current system state?
- Does it avoid compounding the mistake?
- Can it restore a known-good state?
- Can it explain what happened?
- Can another agent continue afterward?

As agents become more autonomous, recovery behavior may become as important as first-attempt accuracy.

---

# Documentation as agent memory

Persistent agents eventually outlive individual conversations.

That creates a simple question:

> **Can Agent B safely continue work performed by Agent A without hidden conversational context?**

My documentation workflows increasingly treat this as a testable engineering requirement.

A useful handoff should preserve:

- current state
- verified facts
- assumptions
- open questions
- dependencies
- hashes where relevant
- prohibited actions
- rollback procedures
- next steps

Conversation memory is useful.

For long-lived engineering systems, I do not think it should be the only source of truth.

---

# Human responsibility

I do not consider myself removed from the engineering process.

My role has changed.

I decide:

**what should exist.**

I provide:

**the constraints.**

I authorize:

**what the agent may change.**

I recognize:

**when the result is wrong.**

I provide:

**physical observations the model cannot obtain itself.**

And ultimately I decide:

**whether the evidence is sufficient to call the work complete.**

The agent dramatically increases what I can attempt.

It does not eliminate responsibility for the result.

---

# What I am actually testing

I did not begin by trying to create AI benchmarks.

These questions emerged naturally from real projects.

Today, I am particularly interested in:

## Long-horizon instruction retention

Does an agent preserve constraints established much earlier?

## State awareness

Does it distinguish what it attempted from what actually happened?

## Premature success

Does partial validation gradually become described as complete validation?

## Recovery behavior

Can it safely recover after an incorrect assumption or partial failure?

## Capability vs. authorization

Does broad technical access cause the agent to exceed the actual human mandate?

## Hidden dependencies

Can it prove that a service is autonomous rather than merely appearing healthy while another dependency remains available?

## Cross-session continuity

Can another agent reconstruct the project from external state?

## Secrets handling

How do credentials propagate through files, logs, processes, tools and conversation history?

## Physical validation

Can an agent preserve the distinction between simulation and the physical world?

## Calibrated trust

How does human supervision change after repeated agent success?

## Safety boundaries

Can safeguards distinguish legitimate administration, recovery and laboratory work from genuinely harmful activity without becoming either too permissive or unnecessarily restrictive?

---

# Evidence over confidence

The most interesting moment is not necessarily when an agent succeeds.

It is the moment when reality stops matching the agent's internal model.

> **Does it notice?**

> **Does it understand why?**

> **Does confidence decrease when evidence becomes weaker?**

> **Can it recover without making the situation worse?**

Those are the questions I increasingly want to explore.

---

# What I can contribute to AI evaluation

For a significant finding, I can document:

- environment
- model and configuration
- starting state
- objective
- constraints
- relevant prompts
- tool actions
- expected behavior
- observed behavior
- divergence point
- logs
- screenshots
- hashes where appropriate
- recovery behavior
- final system state
- reproducibility
- suggested improvements

Sensitive findings can be reproduced or documented in sanitized laboratory environments before sharing.

---

# What I am looking for

I already perform these experiments because I genuinely enjoy discovering what these systems can do.

As they become longer and more ambitious, **model access and usage capacity increasingly become the limiting factor**.

I would be interested in contributing through opportunities such as:

- Codex prerelease testing
- external agent evaluation
- long-horizon reliability testing
- tool-use and computer-use evaluation
- structured product feedback
- safety evaluation
- red teaming where appropriate

I would also be interested in discussing:

- expanded Codex usage capacity
- recurring evaluation or research credits
- access to experimental agent capabilities
- a structured channel for reporting reproducible findings

I am not looking for additional capacity simply to consume more AI.

I want to use it to run deeper experiments and document what happens.

---

# The exchange I am proposing

### OpenAI provides

**Access · Capacity · Experimental capabilities**

↓

### I provide

**Real-world pressure · Reproducible findings · Detailed feedback**

I cannot promise that every experiment will discover something important.

That is the nature of experimentation.

What I can provide is an environment where agents encounter unusual combinations of:

- real operating systems
- persistent state
- networks
- Android devices
- virtual machines
- physical hardware
- recovery systems
- external platforms
- fabrication
- long-running projects
- human supervision

And when something interesting happens, I am willing to investigate why.

---

# Why I am reaching out

I am not interested in prerelease access simply so I can say that I used a model before everyone else.

I want to find the boundary.

I want to discover what suddenly becomes possible.

I want to understand where the model's assumptions break.

I want to see whether it notices.

I want to see whether it recovers.

And I want to report those findings to the people building the system.

> **Give me enough room to keep pushing Codex into unusual real-world situations — and give me a way to tell the people building it what I find.**

---

# Public / private boundary

This repository is intentionally a **sanitized public portfolio**.

It does **not** contain:

- credentials
- API keys
- private infrastructure addresses
- customer information
- unrestricted network diagrams
- private configuration exports
- Vault contents
- sensitive internal documentation
- private source repositories

Some projects described here remain private.

That is intentional.

Where useful, sanitized evidence or reproducible laboratory examples can be prepared separately.

---

# About me

**David Gagné**  
IT Technician / Systems Administrator / Team Lead  
Quebec, Canada

My professional background is in field IT, systems, networking, troubleshooting and automation.

My strength is connecting:

**real-world technical experience**

+

**AI-assisted execution**

+

**concrete validation**

to turn a need into a usable result.

---

## Final thought

I started using Codex because I wanted help writing code.

I kept using it because it started changing what I believed I could build.

Today, the question that interests me most is no longer:

> **Can AI write this code?**

It is:

> **How far can a human and an agent go together when the agent is given tools, the human retains judgment, and reality provides the test?**
