---
title: Open Workflow Specification 1.1.0 Released
author: Open Workflow Specification Contributors
date: 2026-11-12
description: >
  Open Workflow Specification 1.1.0 is here, with new workflow capabilities, runtime behavior clarifications, and a migration guide.
---

We’re pleased to announce **Open Workflow Specification 1.1.0**. This release adds new ways to connect workflows to agent protocols, run processes, and control scheduling, while clarifying runtime behavior across the specification.

## What’s new

- **Agent protocol calls:** workflows can call Model Context Protocol (MCP) servers and Agent-to-Agent (A2A) agents.
- **More process controls:** container tasks support standard input, arguments, and image pull policies; script and shell tasks gain standard input, and shell tasks can set a working directory.
- **Scheduling and iteration:** schedules can select whether to read event data, its envelope, or the raw event, and `for.in` accepts inline arrays.
- **More precise flow and expression behavior:** `try.catch.then` controls the error path, duration can be a runtime expression, and jq output mapping and expression evaluation rules are clarified.

The release also includes changes that may require migration, including `run.shell.arguments` becoming an array, lifecycle completion events using `outputUri`, and the schema moving to YAML only. Review the [upgrade guide](https://github.com/open-workflow-specification/specification/blob/v1.1.0/docs/upgrade-to-1.1.0.md) for breaking changes, deprecations, and upgrade checklists.

The **[v1.1.0 YAML schema](/schemas/1.1.0/workflow.yaml)** is available on the website. See the complete [v1.1.0 release notes](https://github.com/open-workflow-specification/specification/releases/tag/v1.1.0) for details.
