# Investigate Scan Issue

An agent skill that reviews one existing static-analysis finding for defensive remediation. It weighs supporting evidence and counterevidence, then returns a scoped disposition for a human reviewer: `confirmed`, `refuted`, `dependent`, or `unresolved`.

## Use the skill

Use [`SKILL.md`](SKILL.md) in your agent’s skill directory under `investigate-scan-issue/`. Provide the original finding and the handoff from [Prepare Scan Slice](https://github.com/rafik-mikhail/prepare-scan-slice), or provide the finding and relevant authorized source excerpts directly. You can paste them into the prompt or point the agent to the files.

The review is source-only. The skill does not run code or scans, create reproducers, modify source, or close alerts.

## Use as agent instructions

Copy the [Investigate Scan Issue instruction gist](https://gist.github.com/rafik-mikhail/4b06cca6c31c9661cc29cf7e61079983) into your agent’s instruction file. The gist contains the same guidance with `applyTo: "**"` front matter for tools that support it. If your agent accepts plain Markdown instructions, copy the body without the front matter.

## How to test

Follow the [evaluation guide](TESTING.md). It covers the four dispositions, evidence grounding, incorrect dismissals, and repeat-run stability.
