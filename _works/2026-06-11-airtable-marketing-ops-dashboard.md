---
title: Airtable Marketing Ops Dashboard
description: How I replaced a chaotic, multi-spreadsheet operation with a centralized Airtable system — relational databases, role-based views, and automations that scale across a 150+ site network.
category: Marketing Operations
date: 2026-06-11 09:00:00 +0000
role: Marketing Systems Engineer
image: /images/airtable-dashboard.jpg
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin-bottom:36px;border-radius:8px;">
  <iframe src="https://www.youtube.com/embed/JHxcg2C4sLs" title="Airtable Marketing Ops Dashboard — Case Study" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
</div>

A client was running a large-scale content operation — a network of **150+ sites** in an extremely competitive niche — and trying to manage the whole thing with a pile of disconnected spreadsheets. As they put it, it had become a chaotic, jumbled mess. I rebuilt it into a smooth, scalable marketing machine.

The specifics of *their* niche don't matter much. Any marketing operation with repeatable processes, multiple team members, and complex interconnected workflows hits the exact same wall — and this is how I tore it down.

## The workflow they were drowning in

Running the network meant coordinating five interlocking stages across hundreds of properties:

1. **Domain acquisition** — sourcing newly available domains and storing registration credentials, renewal dates, and core metadata.
2. **Technical setup** — hosting configuration, WordPress installs, themes, base pages.
3. **Content planning** — topic, keyword targets, and publishing cadence for each site.
4. **Internal linking** — mapping relationships across the portfolio and tracking anchors so the structure stayed clean.
5. **QA & maintenance** — indexation checks, uptime, publishing consistency, and a long recurring checklist.

Now picture coordinating all of that across hundreds of properties and multiple teammates using nothing but spreadsheets. It broke down in five predictable ways.

## The five problems

- **The information treasure hunt.** Nobody knew which spreadsheet held what. A simple question — *which sites need content this week?* — could take an hour to answer.
- **No single source of truth.** The same record lived in multiple sheets that didn't agree. "Setup complete" here, "in progress" there. Duplicate work, constant conflicts.
- **Zero operational visibility.** Management had no bird's-eye view. They couldn't answer *how many sites are live right now?* — they were flying blind.
- **Scattered communication.** Context lived in Slack threads, email, and random spreadsheet-cell comments. Decisions and history were impossible to reconstruct.
- **Manual, repetitive busywork.** Every publish meant hand-updating a content sheet, a status sheet, and a QA sheet. Hours a week lost to data entry instead of strategy.

It wasn't just inefficient — it was unsustainable. So I didn't "switch them to Airtable." I redesigned the entire operational system from the ground up.

## What I built

**A relational database architecture.** Instead of five isolated spreadsheets, a set of interconnected tables with a central **Domains** hub linked to **Backlinks**, **Team Members**, **Tasks**, and more. Real relationships (one domain → many backlinks; one task → many people) mean a single update propagates everywhere — change a hosting provider once and it's correct in every view, task, and report that references it.

**Custom views for every role.** Same data, displayed for the job at hand. A setup view exposing only setup-relevant fields. A manager's content-pipeline view showing exactly which sites need content and what stage they're in. A permission-gated QA dashboard sorted by priority. A team-workload view showing who's overloaded and who has capacity. Everyone sees their slice instead of staring at one giant sheet.

**Centralized communication.** Every domain became a record with a full history — comments, @-mentions, attached screenshots and docs, and a complete timeline. *"Why did we set it up this way?"* is now answered in the record, not by digging through Slack.

**Automated workflows — the part I'm proudest of.** The dashboard orchestrates the rest of the stack:

- When a domain is added and hits a given status, tasks are **auto-created and assigned** to the right people in ClickUp.
- Every 24 hours the system calls the **WordPress API** for each site to pull its latest post date, then a formula field flags exactly which sites need fresh content — replacing a manual check across hundreds of domains.

## The outcome

The operation went from an hour-long scavenger hunt for basic answers to real-time visibility, a single source of truth, and recurring busywork collapsed into one-click (or zero-click) automations. The team got their time back for strategy — and the system held up as the network scaled past 150 sites.

The pattern travels: relational data, role-based views, centralized context, and automation-first design will fix almost any marketing operation that's outgrown its spreadsheets. **If that sounds like your team, this is the kind of system I build.**
