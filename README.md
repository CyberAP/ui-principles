# UI principles

18 numbered design principles for interactive interfaces: what goes on a
surface, how it behaves, how it looks. What they cover, and what they don't,
is the opening of [`SKILL.md`](SKILL.md).

## Install

It is a skill: the directory is the unit, `SKILL.md` is the entry point.
Copy or symlink it where the harness looks for skills.

    cp -r ui-principles ~/.claude/skills/     # every project
    cp -r ui-principles .claude/skills/       # this project only

The description is what makes it fire — the agent reaches the principles on
its own during UI work, instead of someone remembering the file.

## Without a skill system

Copy `SKILL.md` into the project as a plain document and point the file the
harness already loads at it:

```md
<!-- AGENTS.md / CLAUDE.md -->
- UI work — designing, building or reviewing any interface — follows
  `docs/ui-principles.md`.
```

Scope the line to UI work. An unconditional "read this on every task" is
paid for on every turn and gets skimmed; a scoped trigger is acted on.

## License

CC0 1.0 (public domain) — see [`LICENSE`](LICENSE).
