# Using local skills (`.agent/skills`) ✅

Place skill folders inside a top-level hidden folder named `.agent/skills` so your agent can discover and use them.

## Quick start
1. Create the skills directory:

```bash
mkdir -p .agent/skills
```

2. Copy a skill into the folder (example uses an existing skill directory in this repo):

```bash
cp -r ai-engineer .agent/skills/
```

3. Verify the skill is present:

```bash
ls -1 .agent/skills
```

4. Restart or reload your agent so it picks up the new skill (agent-specific).

---

## Recommended skill layout 🔧
- `.agent/skills/<skill-name>/`
  - `README.md` — short description + usage
  - `manifest.json` or `skill.yml` (optional metadata)
  - implementation files (scripts, handlers, prompts)

## Development tips 💡
- Work on a skill in-place and link it into `.agent/skills`:

```bash
ln -s "$PWD/ai-engineer" .agent/skills/ai-engineer
```

- To keep local skills out of Git, add `.agent/skills/` to your `.gitignore`.

> Note: how skills are loaded (auto-reload vs restart) depends on your agent runtime—check its docs.

## Contributing
- Add a `README.md` inside each skill folder describing purpose and usage.

---
