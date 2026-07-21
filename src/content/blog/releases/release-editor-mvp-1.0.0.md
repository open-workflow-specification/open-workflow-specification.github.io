---
title: Announcing the Open Workflow Specification Diagram Editor (MVP)
author: Lorna Kelly
date: 2026-07-21
description: >
  The first MVP release of the Open Workflow Diagram Editor - a React component that turns your workflow definitions into interactive diagrams. Compatible with Specification 1.0.0.
---

🎉 We're excited to share the first **MVP release** of the [**Open Workflow Diagram Editor**](https://www.npmjs.com/package/@openworkflowspec/diagram-editor) — a new React component that renders your Open Workflow definitions as interactive diagrams. It's the first step toward a full visual editing experience for the Open Workflow ecosystem, and it's ready for you to try today.

## What is the Diagram Editor?

The Diagram Editor (`@openworkflowspec/diagram-editor`) is a React component that takes a **Open Workflow Specification 1.0.0** definition - in YAML or JSON - and visualizes it as an interactive, automatically laid-out diagram.

It's built on top of the tools the community already knows:

- The **[Open Workflow TypeScript SDK](https://github.com/open-workflow-specification/sdk-typescript)** for parsing and understanding workflow definitions.
- **[React Flow (`@xyflow/react`)](https://reactflow.dev/)** for diagram rendering and interaction.
- **[ELK](https://www.eclipse.org/elk/)** for automatic graph layout, so your workflows are arranged cleanly without any manual positioning.

## What's in the MVP

This first release focuses on **visualizing** workflows. Here's what you get:

- ✅ **Spec 1.0.0 support** - render any Open Workflow 1.0.0 definition straight from YAML or JSON.
- ✅ **Interactive diagram** - pan, zoom, and explore your workflow with automatic layout.
- ✅ **Light / dark / system color modes** — the editor adapts to your application's theme.
- ✅ **Internationalization** — built-in support for multiple locales (English only to start).
- ✅ **Modern React component** — a React 19 component you can embed into your own apps.
- ✅ **Schema validation** — definitions are checked against the Open Workflow 1.0.0 schema, with clear feedback when something doesn't conform.
- ✅ **Graceful error handling** — clear parsing-error feedback when a definition can't be rendered.

## A quick look

The component takes your workflow definition as a string and renders it:

```tsx
import { DiagramEditor } from "@openworkflowspec/diagram-editor";
import "@openworkflowspec/diagram-editor/styles.css";

const workflow = `
document:
  dsl: '1.0.0'
  namespace: default
  name: hello-world
  version: '1.0.0'
do:
  - step1:
      set:
        message: hello world
`;

export function App() {
  return (
    <DiagramEditor
      content={workflow}
      isReadOnly={true}
      locale="en"
      colorMode="system"
    />
  );
}
```

> **Note:** This MVP is focused on visualization. Interactive, in-place editing of workflows is on the roadmap — for now, `isReadOnly` keeps the experience clear and predictable.

## Try it now

The Diagram Editor is available on npm:

```bash
npm install @openworkflowspec/diagram-editor
# or
pnpm add @openworkflowspec/diagram-editor
# or
yarn add @openworkflowspec/diagram-editor
```

Then drop the component into your app as shown above.

Prefer to explore the source or see it running end to end? Clone the repository and launch the live Storybook demo, which comes with example workflows and use cases so you can see the component in action and explore the API:

```bash
# Clone the repository
git clone https://github.com/open-workflow-specification/editor.git
cd editor

# Install dependencies (Node.js 22, pnpm 10.31.0)
pnpm install

# Build the packages
pnpm run build:dev

# Run the Storybook demo for the diagram editor
cd packages/open-workflow-diagram-editor
pnpm run start
```

## What's next

This MVP is just the beginning. On the roadmap:

- ✏️ **Interactive editing** — moving from visualization to a full visual editor.
- 🔀 **Dual text + diagram editor** — edit your workflow as text, with both views kept in sync.
- 🧩 **VS Code extension** — bringing the editor into your IDE.

## Get involved

The Open Workflow Diagram Editor is an open, community-driven project, and we'd love your feedback, ideas, and contributions.

- ➜ **Explore the code**: [open-workflow-specification/editor](https://github.com/open-workflow-specification/editor)
- ➜ **Report issues or request features**: [editor issues](https://github.com/open-workflow-specification/editor/issues)

Happy coding! 🚀
