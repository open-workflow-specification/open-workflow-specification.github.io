---
title: "Open Workflow SDK Go 4.0.0"
author: "Ricardo Zanini"
date: "2026-07-14"
description: >-
  Open Workflow SDK Go 4.0.0 is here — the Go SDK moves to its new home under the Open Workflow Specification organization with a fresh module path and updated branding.
---

## Announcing the Release of Open Workflow SDK Go 4.0.0

We are excited to announce **Go SDK 4.0.0**, the first release under the **Open Workflow Specification** organization. This release marks the project's transition from "Serverless Workflow" to **Open Workflow**, reflecting the broader scope of the specification.

👉 Full release notes: [GitHub – v4.0.0](https://github.com/open-workflow-specification/sdk-go/releases/tag/v4.0.0)

---

## What's New in 4.0.0?

This release focuses on the rebranding — there are **no API or schema changes** from the v3.x line. The specification conformance remains at **v1.0.0**.

### New GitHub Home

The SDK now lives at [github.com/open-workflow-specification/sdk-go](https://github.com/open-workflow-specification/sdk-go). GitHub redirects from the old URL are in place, so existing links and references to v3.x releases continue to work.

### Updated Go Module Path

The module path has changed to reflect the new organization:

```
github.com/open-workflow-specification/sdk-go/v4
```

### Updated Error Type URIs

Standard error type URIs now use the `open-workflow-specification.org` domain:

```
https://open-workflow-specification.org/spec/1.0.0/errors/validation
https://open-workflow-specification.org/spec/1.0.0/errors/authentication
...
```

---

## Migration Guide

Upgrading from v3.x is straightforward — update your imports and run `go get`:

1. Update your import paths:

   ```go
   // Before
   import "github.com/serverlessworkflow/sdk-go/v3/parser"
   import "github.com/serverlessworkflow/sdk-go/v3/impl"

   // After
   import "github.com/open-workflow-specification/sdk-go/v4/parser"
   import "github.com/open-workflow-specification/sdk-go/v4/impl"
   ```

2. Fetch the new module:

   ```bash
   go get github.com/open-workflow-specification/sdk-go/v4
   ```

3. If your code references error type URIs (e.g., `https://serverlessworkflow.io/spec/1.0.0/errors/...`), update them to `https://open-workflow-specification.org/spec/1.0.0/errors/...`.

4. Run your tests to verify the transition:

   ```bash
   go test ./...
   ```

---

## What's Next

The reference implementation continues to grow. Check out the [implementation roadmap](https://github.com/open-workflow-specification/sdk-go#implementation-roadmap) to see what's supported and where you can contribute.

---

## Community

The project remains under **CNCF** governance. Join us on the CNCF Slack in the `#open-workflow-sdk` channel to collaborate, ask questions, and contribute.

* Issues & feedback: [github.com/open-workflow-specification/sdk-go/issues](https://github.com/open-workflow-specification/sdk-go/issues)
* Specification: [github.com/open-workflow-specification/specification](https://github.com/open-workflow-specification/specification)

Thank you to everyone who contributed to this milestone release!
