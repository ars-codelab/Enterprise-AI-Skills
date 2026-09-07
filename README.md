# Enterprise AI Skills

A growing collection of reusable skills that help you get more done with an AI agent. Each skill is a set of instructions, a framework, and a workflow you can point your AI agent at. This repo started with one skill, and I intend to add more as I find problems worth packaging.

## What is a skill?

A skill is a plain markdown file that tells an AI agent how to do a specific job. You upload a document, point the agent at the skill, and it follows the instructions. No special software, no code to run. If your AI tool supports skills (Claude, opencode, Cursor, and several others do), you drop the folder in and go.

## The Skills

| Skill | What it does |
| --- | --- |
| [AI Proposal Advisor](AI%20Proposal%20Advisor/SKILL.md) | Stress-tests an AI vendor proposal, scores it, and drafts clarifying questions to send back |

---

## AI Proposal Advisor

Most organizations outside of tech do not have the technical background to review an AI vendor proposal on their own. I learned this the hard way. We give trusted partners access to internal information, they find a real business problem, and then they jump straight to the solution. Architecture, roadmap, resourcing, done.

But the hard questions rarely get asked. How is the data protected? What metrics actually improve, and by how much? When does a human stay in the loop? What happens if the model or the vendor changes tomorrow? What does this cost at scale?

This skill fixes that. You upload a vendor proposal and the agent works it against a structured framework of 13 questions across three pillars.

![AI Vendor Proposal Evaluation Framework](AI%20Proposal%20Advisor/assets/framework.png)

### The three pillars

- **Should we build it?** Problem validity, business value, financial return, and technical fit.
- **Can we trust and operate this safely?** Data protection, humans in the loop, accountability, and recovery.
- **Can we sustainably own and improve this?** Enterprise foundations, IP and portability, and long-term improvement.

Each dimension gets scored from 0 to 10. The agent also surfaces the top three blind spots that could derail the project, and it writes 5 to 7 pointed questions you can email straight back to the vendor.

### How to use it

1. Put the `AI Proposal Advisor` folder into your AI tool's skills directory.
2. Upload a vendor proposal, a RFP response, or a solution deck.
3. Say something like: _Review this proposal using the AI Proposal Advisor skill._
4. Review the executive summary, the score, the blind spots, and the questions to send back.

### The POC gate

One rule matters more than any other. If a proposal recommends a pilot, the agent checks for clear exit criteria. Defined pass criteria, defined fail criteria, and pre-agreed next steps. A pilot without that is just an expensive, slow-motion proposal.

---

## Notes

- Not every question can be answered at proposal stage, and that is okay. Some things only become clear through a pilot. The skill tells you which ones need a POC and how to define success before you start.
- The framework is designed to be used before you sign a contract or commit capital, not after.

## Contributing

Found a gap in a framework or a better question to ask? Open an issue or submit a pull request. This is meant to grow with the community.
