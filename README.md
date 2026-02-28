# Microlinux

Founded by **Ahmad Alfuhaed**  
Official Website: https://ahmad.sug-b.com/microlinux/

Microlinux is a research-driven project focused on designing and evaluating an Energy-Aware Scheduler layer for the Linux kernel.

The goal is not to rewrite an operating system from scratch, but to explore a fundamental architectural question:

> What if scheduling decisions were made with energy cost as a first-class parameter?

---

## Project Scope (Phase 1)

Microlinux Phase 1 is strictly limited to:

- Researching Linux scheduler behavior
- Measuring wakeups, context switches, and CPU residency states
- Designing and testing an energy-aware scheduling hook
- Publishing measurable results

This project does NOT currently aim to:

- Replace the Linux kernel
- Build a full microkernel
- Re-implement drivers
- Target commercial devices

We begin with research discipline and measurable outcomes.

---

## Technical Direction

Base system: Linux kernel  
Language: C  
Focus area: Scheduler & Energy Behavior  
Tools: perf, ftrace, powertop (initially)

---

## Why This Matters

Modern systems operate under strict energy constraints:
- Mobile devices
- Edge computing
- Embedded systems
- Aging hardware

Current schedulers prioritize fairness and performance.
Microlinux explores whether energy cost can become a scheduling primitive.

---

## Repository Structure

---

## Founder

Ahmad Alfuhaed  
Project Founder & Vision Architect  

Official project page:  
https://ahmad.sug-b.com/microlinux/
