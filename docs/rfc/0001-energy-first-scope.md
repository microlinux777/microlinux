# RFC-0001
## Energy-First Scheduler Research Scope

Status: Draft  
Author: Microlinux  
Date: 2026-03-01  

---

## 1. Purpose

This RFC defines the initial research scope of Microlinux Phase 1.

The purpose is to evaluate whether an Energy-Aware Scheduling layer can measurably reduce unnecessary CPU wakeups and improve energy efficiency in Linux-based systems.

---

## 2. Problem Statement

Modern Linux schedulers are primarily designed around:

- Fairness
- Throughput
- Responsiveness

Energy behavior is handled mostly through reactive mechanisms such as CPU frequency scaling and idle states.

This creates a structural limitation:

Scheduling decisions do not directly incorporate estimated energy cost.

---

## 3. Phase 1 Objectives

Phase 1 will focus on:

1. Mapping the wakeup path inside the Linux scheduler.
2. Measuring:
   - Number of wakeups
   - Context switches
   - CPU residency states
3. Identifying points where energy-aware hooks could be introduced.
4. Implementing an experimental scheduler modification.
5. Benchmarking against baseline Linux behavior.

---

## 4. Non-Goals

The following are explicitly out of scope:

- Rewriting the Linux kernel
- Building a new microkernel
- Replacing drivers
- AI-based scheduling
- Hardware reverse engineering

Scope discipline is mandatory.

---

## 5. Research Questions

1. Can wakeups be reduced without degrading responsiveness?
2. Can energy cost estimation influence scheduling priority?
3. What is the measurable tradeoff between fairness and energy savings?

---

## 6. Measurement Strategy

Initial tools:

- perf
- ftrace
- powertop

Target metrics:

- Wakeups per second
- Context switches per second
- CPU idle residency percentage
- Energy usage (where measurable)

---

## 7. Success Criteria

Phase 1 is considered successful if:

- A measurable reduction in unnecessary wakeups is demonstrated.
- Energy savings are observable under controlled workload.
- Results are reproducible and documented.

---

## 8. Next Steps

- Select target Linux kernel version
- Select hardware test platform
- Begin wakeup path tracing

End of RFC-0001
