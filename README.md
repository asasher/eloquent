# Asher Skills

One installable career-development skill for AI coding agents. It consolidates the former multi-skill ResumeSkills content into a single entry point, `resume-skills`, with focused subcommands.

## Structure

```text
skills/resume-skills/
+-- SKILL.md
+-- agents/
|   `-- openai.yaml
+-- reference/
|   +-- resume-ats-optimizer.md
|   +-- resume-bullet-writer.md
|   `-- ...
`-- scripts/
    `-- command-metadata.json
```

`SKILL.md` is the only trigger surface. The detailed workflows live in `reference/` and are loaded only when the matching subcommand is used.

## Install

Install globally:

```bash
npx skills add asasher/asher-skills -g -y
```

Install in the current project:

```bash
npx skills add asasher/asher-skills -y
```

## Usage

Invoke the single skill directly or ask naturally:

```text
resume-skills ats
resume-skills bullets
resume-skills analyze-job
resume-skills tailor
resume-skills cover-letter
resume-skills interview
resume-skills salary
```

Natural requests route to the nearest subcommand:

```text
"Optimize this resume for ATS."
"Rewrite these bullets for a senior product role."
"Here is a job description and my resume. Should I apply?"
"Tailor my resume for this posting."
"Write a cover letter for this role."
```

## Commands

| Command | Purpose |
|---|---|
| `ats` | ATS compatibility, parsing risk, keywords, and formatting |
| `bullets` | Achievement-focused resume bullet rewriting |
| `quantify` | Credible metrics, scale, and impact discovery |
| `format` | Resume layout, readability, and ATS-safe structure |
| `sections` | Summaries, skills, experience, education, and extra sections |
| `analyze-job` | Job description analysis, fit scoring, and application strategy |
| `tailor` | Job-specific resume customization |
| `versions` | Master resume and tailored version management |
| `cover-letter` | Personalized cover letters |
| `linkedin` | LinkedIn profile optimization |
| `portfolio-case-study` | Portfolio case studies from resume/project material |
| `references` | Professional reference lists and prep notes |
| `interview` | STAR stories, likely questions, and interview prep |
| `salary` | Compensation research and negotiation scripts |
| `compare-offers` | Side-by-side offer comparison |
| `tech` | Technical resumes for SWE, PM, data, DevOps, and related roles |
| `executive` | VP, C-suite, board, and senior leadership resumes |
| `academic-cv` | Academic CVs for faculty, research, postdoc, and teaching roles |
| `creative` | Creative resumes balanced with ATS compatibility |
| `career-change` | Transferable skill translation for career pivots |

## Design

The skill follows the same broad shape as `impeccable`: one entrypoint, a command table, routing rules, detailed command references, and command metadata. This keeps activation predictable and avoids installing twenty separate skills for related resume workflows.

## License

MIT. See [LICENSE](LICENSE).
