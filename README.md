# MimiK

MimiK is a **collection of small, independent, cross-MCU C implementations of common primitives**.

That’s all it is.

No framework.
No runtime.
No system.
No opinionated structure.

Just code.

---

## What this repo contains

This repo contains **pure C (C99) implementations** of things like:

* memory allocation helpers (`kmalloc`, `mfree`, fixed blocks, simple heaps)
* mutexes
* semaphores
* spinlocks
* queues
* ring buffers
* linked lists
* small utility primitives

Each component is **standalone**.
You can take one file and ignore the rest.

---

## Scope

* Written in **plain C**
* No architecture-specific instructions
* No CMSIS
* No vendor SDKs
* No compiler extensions
* No assumptions about interrupts, cores, or scheduling

If something requires platform-specific behavior, it is exposed as a **hook** and left for the user to define.

---

## What this is NOT

* Not an RTOS
* Not a kernel
* Not a library ecosystem
* Not an SDK
* Not a portability layer

This repo does **not** try to abstract hardware.
It does **not** try to unify platforms.
It does **not** try to be clever.

---

## Why this exists

This repo exists because:

* Platform SDKs provide useful primitives, but they are **platform-locked**
* Sometimes you want the same primitive on **different MCUs**
* Sometimes you want it in **plain C**, without dragging an SDK with it

That’s the entire reason.

---

## Design constraints

* Every file should be readable in isolation
* No hidden behavior
* No global policy decisions
* No pretending this works everywhere without adaptation

The goal is **maximum mechanical portability**, not automatic portability.

---

## Intended use

* Copy files into your project
* Modify them
* Delete what you don’t need
* Adapt hooks to your environment
* Forget this repo exists

There is no required way to use MimiK.

---

## Vision (yes, it’s still dumb)

This is a dumb project.

It does not solve a hard problem.
It does not introduce new ideas.

The goal is simply to have **cross-MCU, pure-C implementations of primitives** that can be reused across projects.

---

## License

Use it however you want.
Change it. Break it. Ship it.

---
