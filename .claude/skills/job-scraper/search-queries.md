# Search Queries for Job Scraper

<!-- SETUP: Customize these queries based on your skills, target roles, and location -->

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Shipped country-agnostic CLIs include `linkedin-search` and `freehire-search`; Danish demos and any skill you add with `/add-portal` are included the same way. You do **not** need a matching `site:` line below for those CLIs to run.

The `site:` query templates in this file are the **WebSearch fallback** — for portals without a CLI, company career pages, or when a CLI fails.

**Language scope:** English.

## Search Sites

Primary:
- **linkedin.com/jobs** - LinkedIn job listings (filter: United States / St. Louis, MO area); also covered by `linkedin-search` CLI
- **indeed.com** - Indeed job listings (filter: St. Louis, MO / Remote)

Secondary (company career pages via Google):
- Direct Google searches with `site:` filters for known target companies (e.g. Spectrum/Charter, Publix, various tech/SaaS companies).

## Query Categories

Queries are grouped by priority. Combine each query with your location terms (e.g. Saint Peters, St. Louis, or Remote) where the site supports it.

### Priority 1: Quality Engineering Manager / QA Lead

These match your strongest and most desired career direction.

```
site:linkedin.com/jobs "Quality Engineering Manager" "St. Louis"
site:linkedin.com/jobs "Quality Engineering Manager" "New York"
site:linkedin.com/jobs "Quality Engineering Manager" "San Francisco"
site:linkedin.com/jobs "Quality Engineering Manager" "San Diego"
site:linkedin.com/jobs "Quality Engineering Manager" "Austin"
site:linkedin.com/jobs "Quality Engineering Manager" Remote
site:linkedin.com/jobs "QA Lead" "St. Louis"
site:linkedin.com/jobs "QA Lead" "New York"
site:linkedin.com/jobs "QA Lead" "New Jersey"
site:linkedin.com/jobs "QA Lead" "San Francisco"
site:linkedin.com/jobs "QA Lead" "Austin"
site:linkedin.com/jobs "QA Manager" "St. Louis"
```

### Priority 2: Release Readiness & Build Quality

These match your domain expertise.

```
site:linkedin.com/jobs "Release Manager" "St. Louis"
site:linkedin.com/jobs "Release Manager" "New York"
site:linkedin.com/jobs "Release Manager" "San Francisco"
site:linkedin.com/jobs "Release Manager" "Austin"
site:linkedin.com/jobs "Build Readiness" "QA"
site:linkedin.com/jobs "Release QA Lead" "St. Louis"
```

### Priority 3: Senior QA Automation Engineer

Adjacent roles you could pivot into or target as secondary options.

```
site:linkedin.com/jobs "Senior QA Automation Engineer" "Playwright" "St. Louis"
site:linkedin.com/jobs "Senior QA Automation Engineer" "Playwright" "New York"
site:linkedin.com/jobs "Senior QA Automation Engineer" "Playwright" "San Francisco"
site:linkedin.com/jobs "Senior QA Automation Engineer" "Playwright" "Austin"
site:linkedin.com/jobs "Sr. QA Automation" "Python" "St. Louis"
site:linkedin.com/jobs "Lead QA Automation Engineer" Remote
```

### Priority 4: Broader Technical / DevOps / Release

Wider net for general technical roles.

```
site:linkedin.com/jobs "QA Program Lead" "St. Louis"
site:linkedin.com/jobs "Software Engineer in Test" "Python" "St. Louis"
site:linkedin.com/jobs "QA Analyst" "St. Louis"
```

## Location Filter

When evaluating results, verify the job location is within reasonable commute distance or fits your relocation target. Define acceptable areas:
- Saint Peters, MO and Greater St. Louis Metro area
- New York City Metro & New Jersey (relocation preferred)
- San Francisco Bay Area (relocation preferred)
- San Diego, CA (relocation preferred)
- Austin, Texas (relocation preferred)
- Remote (USA)
- Too far: Locations outside these preferred metro areas (requires relocation outside target regions)

## Language Filter

Your working languages and levels are in CLAUDE.md's Languages table. When filtering scraped results, apply `04-job-evaluation.md`'s Language Gate: a posting requiring a language you haven't declared at all is excluded.

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus.
