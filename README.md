# gclbck-crealore-mods

One marketplace for the Claude Code **mods** by Crealore. Add it once, then install any of them.

```sh
claude plugin marketplace add gclbck-crealore/gclbck-crealore-mods
```

Or inside a session: `/plugin marketplace add gclbck-crealore/gclbck-crealore-mods`.

## Mods

| Mod | What it does | Install |
|---|---|---|
| [**is-it-done-yet**](#is-it-done-yet) | A progress pane beside the terminal: percent done, phases and tasks, time, tokens and API cost, read from your project's markdown plan or progress notes, or the agent's task list. | `claude plugin install is-it-done-yet@gclbck-crealore-mods` |
| [**session-handoff-button**](#session-handoff-button) | A Session Hand-off button above the prompt, coloured by context usage; one press writes a handoff, clears and continues in a fresh session, with nothing pasted on screen. Past 65% it warns once. | `claude plugin install session-handoff-button@gclbck-crealore-mods` |

### is-it-done-yet

<img src="https://raw.githubusercontent.com/gclbck-crealore/is-it-done-yet-mod/main/docs/hero.png" alt="is-it-done-yet: a docked progress pane beside the Claude Code terminal" width="420">

A progress pane for long, multi-phase agent work. In a project that already has a plan, checklist or progress note in its markdown files (found by reading them, whatever they are called) it opens beside the terminal and shows percent done, phases and tasks with green/blue/grey bars, elapsed time, a rough ETA, tokens and the API-equivalent cost. Reach L1 (reads the project's markdown files), nothing added to the model's context.

```sh
claude plugin install is-it-done-yet@gclbck-crealore-mods
```

Source and guide: [gclbck-crealore/is-it-done-yet-mod](https://github.com/gclbck-crealore/is-it-done-yet-mod)

### session-handoff-button

A **Session Hand-off** button above the prompt that changes colour as the context window fills (green, orange, red). One press writes a handoff, saves it to a temp `.md`, runs `/clear` and continues in a fresh session: you see one short message while the handoff goes in as hidden context. Past 65% it stops your next prompt once and recommends the button. Reach L2 (drives Claude: one handoff turn, `/clear`, one prompt; writes one temp file per handoff).

```sh
claude plugin install session-handoff-button@gclbck-crealore-mods
```

Source and guide: [gclbck-crealore/session-handoff-button-mod](https://github.com/gclbck-crealore/session-handoff-button-mod)

After installing, run `/reload-plugins` in an open session, or start a new one.

## How this marketplace works

It holds no mod code, only [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json), which points at the folder of each mod inside its own repository. Each mod repo stays the place for its source, issues and releases, and each can still be added on its own as a marketplace. To pick up new versions: `claude plugin marketplace update gclbck-crealore-mods`.

Every mod here is a Claude Code mod and needs Claude Code 2.1.287 or later. Each mod's README lists what it can reach.

## License

[MIT](LICENSE) © 2026 Crealore. Each mod carries its own MIT license in its repository.
