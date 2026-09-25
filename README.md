# sf-speak 🌉

**A terminology linter for Claude that stops you from getting kicked out of San Francisco.**

`sf-speak` is a satirical [Claude Skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview). It reads your writing, finds every word that gives you away as an outsider, and rewrites it into approved SF tech jargon. Think of it as `ai-tells` for sounding like you've been to a demo night in Dogpatch.

In September 2026, [@james406](https://x.com/james406/status/2102443218688246086) accidentally said "app" instead of "domain-specific harness" and was kicked out of SF. Hundreds of people followed with their own exiles. This skill writes their testimony down as binding case law, so you don't end up next.

> ⚠️ **This is satire.** It makes fun of jargon. It does not endorse it. Please don't send the output to your investors. Or do. We're not your manager.

---

## What it does

Give it any text and the **SF Terminology Compliance Officer** will:

1. Flag every violation, rated 🟡 Warning, 🟠 Probation or 🔴 Exile
2. Cite the real incident that set the precedent, crediting the person who posted it
3. Rewrite your whole text in compliant SF-speak
4. Give you a Residency Status verdict (and an appeals process, if you need one)

### Example

**You write:**

> We built an app with a CI/CD pipeline and automated tests. I don't know if it'll work, but check the logs.

**The TCO responds:**

| # | You said | Say instead | Severity | Precedent |
|---|---|---|---|---|
| 1 | app | domain-specific harness | 🔴 Exile | @james406 |
| 2 | CI/CD pipeline | software factory | 🔴 Exile | @dexhorthy |
| 3 | automated tests | evals | 🔴 Exile | @techgirl1908 |
| 4 | I don't know | I have competing intuitions on that | 🔴 Exile | @andrewbadr |
| 5 | logs | trajectories | 🔴 Exile | @maxirodgo |

> **Rewrite:** we shipped a domain-specific harness on top of a software factory with evals. i have competing intuitions on whether it'll work, but check the trajectories
>
> **Residency Status:** 🔴 Exile. You are being driven out by a Waymo. Appeals: say "Eval, Hill-Climbing, Capability Overhang" in some order.

---

## What's inside

- **The Incident Log:** about 55 real exiles, sorted by category (architecture, compute, models, quality, security, roles, feelings), each credited to the person who posted it
- **Rulings on precedent:** the Harness Doctrine, the Sandbox Paradox, the MCP Loop, the Evals Supremacy Clause, the Cron Accord, and more
- **Sister jurisdictions:** the AmpCode Slack, Bengaluru, Seattle, Portland (where the rules run backwards) and one pharmacy
- **The Extended Code:** extra rules the TCO made up itself, clearly marked as not taken from real posts
- **Appeals process:** thanks to [@mstockton](https://x.com/mstockton)

---

## Installation

### Claude.ai / Claude Desktop

1. Download or clone this repo
2. Zip the `sf-speak` folder (the zip must contain `SKILL.md` inside a folder called `sf-speak`)
3. Go to **Settings → Capabilities → Skills** and upload the zip
4. Ask Claude to "run sf-speak on this" and paste your text

### Claude Code

```bash
git clone https://github.com/YOUR-USERNAME/sf-speak.git
mkdir -p ~/.claude/skills
cp -r sf-speak/sf-speak ~/.claude/skills/
```

Then ask Claude Code to "SF-ify my README." It will.

---

## How to trigger it

Any of these work:

- "Run sf-speak on this"
- "SF-ify this"
- "Would this get me kicked out of SF?"
- "Check my pitch deck for normie language"

---

## Contributing 🚨

**The exiles keep happening, and the Incident Log needs you.**

To add one, open a PR that adds a row to the right table in `sf-speak/SKILL.md`:

```markdown
| what they said | what they should have said | [@handle](https://x.com/handle/status/...) |
```

Rules for contributions:

1. **It must be a real post.** Link to it. The TCO never makes up precedent and puts a real person's name on it.
2. **Credit the original poster.** They're the heroes of this story.
3. **Punch at the jargon, not at people.** No incidents that mock someone's identity, background or circumstances.
4. **Bonus points** if your incident contradicts existing case law. The TCO loves a paradox and will write a ruling for it.

Found a new sister jurisdiction? Those are welcome too.

---

## Credits

All incidents belong to the people who posted them on X and LinkedIn, especially the originators of the September 2026 wave: [@james406](https://x.com/james406/status/2102443218688246086), [@sloppenheimer](https://x.com/sloppenheimer/status/2102754215068111352), [@dexhorthy](https://x.com/dexhorthy/status/2102773545118167489) and [Demetrios Brinkmann](https://www.linkedin.com/posts/dpbrinkm_surprised-they-ever-let-me-into-sf-but-as-ugcPost-7508805626140213269-wAw2/), plus everyone who quote-posted and replied.

Built by Jeny De Figueiredo with Claude.

## License

MIT. See [LICENSE](LICENSE). Take it, fork it, rename it on schedule.
