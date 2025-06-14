---
layout: page
title: Trainings
permalink: /trainings/
image: '/images/trainings.png'
---

***

# Windows Kernel Exploitation

<br>

## Overview

This class is meant to show the approach an exploit developer or bug hunter should take in attacking a previously unknown component in the Windows kernel. The training is primarily focused around labs to teach the students what it takes to exploit a real-world vulnerability.

This class focuses on exploiting CVE-2018-8611 on Windows 10 x64 1809 (RS5), a complex race condition that leads to a use-after-free on the non-paged kernel pool. The vulnerability is in the Kernel Transaction Manager (KTM) driver (`tm.sys`), a component that has not received much public scrutiny.

Even though students will learn a lot about the KTM component, we focus on our approach for analyzing this component as a new kernel component that we had no prior knowledge about. The methodology can be reused for any other unknown kernel components a student may encounter in the future. We do not specifically focus on tricks or techniques for bypassing specific Windows versions mitigations, but rather on the thought process behind exploring functionality to find useful unmitigated code paths and also abusing the bug in ways that allow to build powerful primitives that would facilitate mitigation bypasses.

The tools/VM we provide during this training are generic and can be reused after the class to assist exploiting other Windows kernel vulnerabilities.

Students will be able to put their new knowledge into practice by exploiting other vulnerabilities in KTM on Windows 11 x64 (CVE-2024-43570 and CVE-2024-43535).

<br>

### Key learning objectives

* Setup an efficient Windows kernel debugging environment
* Modern reverse engineering and binary patch diffing
* How to approach exploiting a vulnerability on a previously unknown target
* Step-by-step real-world Windows kernel exploit on Windows 10 1809 (RS5) x64

<br>

### Prerequisite knowledge

* Comfortable with x86/x64 assembly and reversing it
* C knowledge (reading/writing)
* Comfortable with disassemblers/decompilers (IDA, Ghidra, etc) and debuggers (WinDbg, x64dbg, gdb, etc)
* Familiarity with memory corruption exploitation on any OS
* Windows kernel internals basic knowledge

<br>

### Who should attend

* Penetration testers
* Red teamers
* Reverse engineers
* Want to become an exploit developer or bug hunter

<br>

### Hardware/Software requirements

* Base OS: Windows (recommended) or Linux
* Hyper-V/VMware virtualisation software
* At least 80GB of free disk space
* At least 8GB of RAM

***

## Course outline

### Part 1: Debug environment

* Hyper-V/VMWare
* WinDbg
* Ghidra/IDA
* ret-sync
* Visual Studio
* **Lab: Debug environment setup**

<br>

### Part 2: Binary diffing Microsoft updates

* Efficient use of the IDA/Ghidra decompiler to analyze the root cause
* **Lab: Basic binary diffing**

<br>

### Part 3: Kernel Transaction Manager (KTM) basics

* KTM objects and APIs
* KTM internals
* Use of public tools for finding data
* **Lab: KTM experimentation**

<br>

### Part 4: Understanding CVE-2018-8611

* Root cause vs effect
* Planning exploitation strategy
* **Lab: Better binary diffing**
* **Lab: Reaching vulnerable code**
* **Lab: Triggering CVE-2018-8611 in a debugger**

<br>

### Part 5: Exploitation techniques

* Bypassing mitigations
* Windows non-paged pool manipulation
* **Lab: Bad vs good feng shui**
* **Lab: Getting controlled UAF in a debugger**

<br>

### Part 6: More exploitation techniques

* Winning the race without a debugger
* Exploitation strategies
* **Lab: Debugging tricks and race win detection**
* **Lab: Discovering a kernel leak**
* **Lab: Restoring cleaned execution**

<br>

### Part 7: How to escalate privileges

* Write primitive and privilege escalation strategy
* **Lab: Arbitrary read and write primitives with write 0 and PreviousMode primitive**
* **Lab: Privilege escalation**
* Arbitrary increment primitive and PreviousMode limitations
* **Lab: Arbitrary read and write primitives with increment primitive**

***

# Comments

I love teaching vulnerability research and exploit development. The course I teach is all about improving your mental model.

{: .note }
Even the most experienced security researchers don't know everything

Making vulnerability research and exploit development accessible is key in our evolving and challenging world.

{: .note }
"EZSecLab": Vulnerability research and exploit development made easy.

Checkout some of my previous students' comments on the course:

> The course is absolutely stellar and gave me the confidence to do independent security research.

> This was probably the best training I took (so far).

> Showing his approach was invaluable to me.

***

# Online trainings

You will find online some of my trainings:

* [Advanced WinDbg](https://p.ost2.fyi/courses/course-v1:OpenSecurityTraining2+Dbg3011_WinDbg3+2023_v1/about) (Open Security Training, September 2022)
* [Windows Kernel Internals 2](https://p.ost2.fyi/courses/course-v1:OpenSecurityTraining2+Arch2821_Windows_Kernel_Internals_2+2023_v1/about) (Open Security Training, September 2022)
* [Windows Kernel Exploitation: Race Condition + UAF in KTM](https://p.ost2.fyi/courses/course-v1:OpenSecurityTraining2+Exp4011_Windows_Kernel_UAF_KTM+2023_v1/about) (Open Security Training, August 2023)

***

# Why attend an in-person training?

> There is enormous value in attending classes in person even if the full course is available online. The most important benefit is the ability to ask questions [...] and be able to learn the materials much faster.