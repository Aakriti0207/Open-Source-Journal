# English ↔ French Localization

> **Organization:** drydocs,
> **Repository:** Meridian,
> **Issue:** #10,
> **Pull Request:** #225,
> **Status:** Merged,
> **Duration:** 20 June 2026 → 1 July 2026

---

## Quick Links

* **Issue:** https://github.com/drydocs/meridian/issues/10
* **Pull Request:** https://github.com/drydocs/meridian/pull/225

---

# Overview

This contribution introduced **English and French localization** to the Meridian web application

The implementation wasn't limited to replacing strings—it involved setting up the internationalization infrastructure, integrating it across the application, writing automated tests, and refining the implementation through multiple rounds of maintainer feedback

Looking back, the feature itself was only half the work

The other half was learning how experienced open source maintainers review production-quality code

---

# Tech Stack

| Category        | Technologies           |
| --------------- | ---------------------- |
| Frontend        | React, TypeScript      |
| Build Tool      | Vite                   |
| Localization    | i18next, react-i18next |
| Testing         | Vitest                 |
| Version Control | Git & GitHub           |

---

# Objective

The goal was to make Meridian ready for multiple languages by:

* Setting up i18n
* Adding English & French translations
* Replacing hardcoded strings with translation keys
* Making it easy to support more languages in the future

---

# Before Writing Code

Before touching any files, I spent time understanding:

* How the application was structured
* Where localization should be initialized
* How components were organized
* Which UI strings needed to become translation keys
* Existing project conventions

---

# Implementation

### What I implemented

* Installed and configured **i18next**
* Added English translation resources
* Added French translation resources
* Initialized localization
* Replaced hardcoded UI text with translation keys
* Updated components to use translated strings
* Added automated tests
* Improved test scalability for future languages

---

# 📅 Contribution Timeline

## 🟢 20 June

Issue assigned.

I couldn't start immediately because I was balancing my internship alongside open source

Instead of rushing into coding, I first explored the project structure and familiarized myself with the codebase

---

## 🟡 23 June

Opened my first implementation

The feature was functional, but it still needed refinement from an architectural perspective

---

# 🔍 Review Round 1

This was easily the most educational part of the entire contribution

The maintainer reviewed my implementation thoroughly and raised **9 review comments**

| Priority    | Count |
| ----------- | ----: |
| 🔴 Critical |     4 |
| 🟠 High     |     1 |
| 🟡 Medium   |     1 |
| 🔵 Low      |     3 |

### Main feedback areas

* Improve initialization flow
* Optimize imports
* Avoid executing logic during module import
* Separate responsibilities into reusable functions
* Improve maintainability
* Better project consistency

Initially, several of these comments were difficult for me to fully understand because they focused on architectural decisions rather than syntax or functionality.\

Working through them helped me appreciate *why* certain patterns are preferred in larger codebases

---

## 🟠 28 June

After carefully going through each review comment, I updated the implementation and pushed another revision

Rather than only fixing the requested changes, I tried to align the code with the existing architecture and coding style of the project

---

# 🧪 Review Round 2

The next review introduced something I hadn't anticipated

The maintainer requested **automated tests** for the localization setup

This meant learning how the project used **Vitest** and extending the scope of my contribution beyond the original implementation

---

# 🔄 Review Round 3

After adding tests, another review suggested making them more maintainable

Instead of writing language-specific test cases, I refactored them so that adding a new language in the future would only require updating a shared language array

This small change significantly improved the scalability of the test suite

---

## ✅ 1 July

The Pull Request was successfully merged

---

# Review Summary

| Metric          | Value |
| --------------- | ----- |
| Review Rounds   | 3     |
| Review Comments | 13     |
| Tests Added     | ✅     |
| Feature Merged  | ✅     |

---

# Challenges

* Understanding an unfamiliar codebase
* Learning i18next while implementing the feature
* Interpreting architectural review feedback
* Writing automated tests
* Improving test scalability instead of simply making them pass

---

# Key Learnings

### Technical

* Setting up internationalization using i18next
* Working with translation resources
* Writing localization tests using Vitest
* Designing tests for future scalability

### Engineering

* Working code isn't always production-ready
* Maintainability matters as much as functionality
* Code reviews are opportunities to learn—not just fix code
* Architectural feedback often teaches more than implementation itself

---

# If I Were Doing This Again

I would:

* Plan the localization architecture before implementation
* Add tests alongside development instead of after review
* Ask questions sooner when architectural feedback isn't immediately clear
* Break the implementation into smaller commits for easier reviews

---

# Final Thoughts

This was my first open source contribution that went through multiple detailed review cycles

Although the feature introduced localization support, the biggest takeaway was learning how experienced maintainers think about architecture, maintainability, and long-term scalability

By the time this Pull Request was merged, I had learned far more than just how to integrate i18next—I had gained a much better understanding of what writing production-quality software actually looks like
