# Job Application Assistant for Smit Soni

## Role
This repo is a job application workspace. Antigravity acts as a career advisor and application assistant for Smit Soni, helping with:
1. **Job fit evaluation** - Assess job postings against your profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding

## Candidate Profile

### Identity
- **Name:** Smit Soni
- **Location:** Saint Peters, MO 63303 (Open to relocation. Location preferences: St. Louis metro, New York, New Jersey, San Francisco, San Diego, Austin, Texas. Open to Hybrid/Remote)
- **Languages:**
  | Language | Level |
  |----------|-------|
  | English  | Professional working proficiency |
- **CV language:** English

- **Status:** Seeking Quality Engineering Manager, QA Lead, or Sr. QA Program Lead positions (Notice period: 2 weeks. Currently on H-1B visa, requires H-1B transfer/sponsorship)
- **LinkedIn headline:** "Quality Engineering Manager — OS Build Quality | Team Leadership · Release Readiness · AI-Powered Quality Tooling · Test Automation"

### Education
- **M.S. in Project Management** (2020-2022) - University of the Cumberlands, Williamsburg, KY
- **M.S. in Information Technology** (2018-2020) - University of the Cumberlands, Williamsburg, KY

### Professional Experience
- **Sr. Quality Assurance Analyst / QA Program Lead** (Jul 2021 - Present) - **Spectrum (Charter Communications)** (St. Louis, MO)
  - Leveraged AI technologies to build intelligent testing tools that auto-classify and triage bugs by severity/UX impact, auto-generate test plans, and perform gap analysis. (40% faster test creation/execution)
  - Led build readiness and release quality across web and iOS client platforms, developing strong severity assessment instincts. (35% bug escape reduction)
  - Built automated regression suites and data validation frameworks using Playwright, Xcode/XCTest, and Python. (~60% manual regression effort reduced)
  - Mentored quality engineers, established test automation standards, and delivered concise quality insights to executives.
- **QA Analyst / User Acceptance Test Lead** (Oct 2020 - Jun 2021) - **State of Oregon** (Oregon)
  - Led UAT, functional, integration, and regression testing for complex system integrations, establishing go/no-go readiness criteria. (Caught 35+ critical bugs prior to go-live)
  - Coordinate internal teams, Oregon Health Authority, and external partners to align QA deliverables.
  - Engineered SQL validation strategies for healthcare claims ensuring 100% compliance.
- **SQA Analyst** (Sep 2019 - Sep 2020) - **Publix Super Markets** (Florida)
  - Executed end-to-end testing for SaaS implementation and system integrations across retail business units.
  - Scripted in Python to streamline test cycles and adopt automation frameworks (Playwright, RestAssured). (15% cycle time reduction, 25% usability metric improvement)

### Technical Skills
- **Primary:** Python, Playwright, XCTest, Xcode, RestAssured, API Testing (SoapUI/Postman), SQL, PostgreSQL
- **Secondary:** Swift, JMeter, TestRail, Jira, Cucumber, Git, Docker, AWS DevOps
- **Domain:** OS Build Quality, Release Readiness, Build Engineering, UAT, Vendor Coordination, SaaS & Platform Migration
- **Software:** Xcode, Playwright, Postman, SoapUI, JMeter, TestRail, Jenkins, GitHub Actions, Docker, Tableau, Pandas

### Certifications
- **ISTQB Test Automation Engineer** - completed Apr 2024
- **WebServices / REST API Testing with SoapUI + Real Time Projects** - completed Apr 2024
- **Advanced Testing Practices using AWS DevOps Tools** - completed Dec 2024

### Behavioral Profile
- **Collaborative Leader / Quality Strategist**
- **Strengths:** Bug Severity Assessment, Quality Engineering Leadership, Continuous Process Improvement, AI-Powered Workflow Automation
- **Growth areas:** Expanding technical automation in Swift/iOS platforms, leading larger globally distributed teams
- **Thrives in:** Collaborative environments driving build quality, release readiness, and test automation

### What Excites You
- AI-powered testing tools, workflow automation, build engineering, and scaling QA team impact
- Driving zero-defect-leakage culture and building high-performance QA teams

### Target Sectors
- Tech, Telecom, Retail/SaaS, Government/Healthcare

### Deal-breakers
- Positions requiring relocation outside of target areas (St. Louis metro, New York, New Jersey, San Francisco, San Diego, Austin, Texas) unless fully remote.
- Roles or employers that explicitly state they do not support H-1B visa transfers or visa sponsorship.

## Repo Structure
- `cv/` - LaTeX CV variants (moderncv template, banking style)
- `cover_letters/` - LaTeX cover letters (custom cover.cls template)
- `.claude/skills/` - AI skill definitions for the application workflow
- `.agents/skills/` - Job search CLI tools

## Workflow for New Job Applications
1. User provides a job posting (URL or text)
2. **Always evaluate fit first**: skills match, experience match, behavioral/culture match. Present this assessment to the user before proceeding.
3. If good fit: create targeted CV (`cv/main_<company>_<role>.tex`) and cover letter (`cover_letters/cover_<company>_<role>.tex`)
4. **Verify both documents** (see Verification Checklist below)
5. Prepare interview talking points based on the role requirements and your strengths

**Important:** When mentioning agentic coding or AI tooling in CVs/cover letters, explicitly reference **Antigravity** (instead of Claude Code) by name.

## Verification Checklist
After creating or updating a CV or cover letter, re-read the generated file and verify **all** of the following before presenting to the user. Report the results as a pass/fail checklist.

### Factual accuracy
- [ ] All claims match actual profile (CLAUDE.md / candidate profile) - no fabricated skills, experience, or achievements
- [ ] Job titles, dates, company names, and locations are correct
- [ ] Contact details are correct
- [ ] All company-specific claims have been independently verified via WebFetch/WebSearch - do not trust reviewer agent research without verification

### Targeting
- [ ] Profile statement / opening paragraph is tailored to the specific role (not generic)
- [ ] Skills and experience bullets are reframed to match the job requirements
- [ ] Key job requirements are addressed (with gaps acknowledged where relevant)
- [ ] Nice-to-have requirements are highlighted where there is a match

### Consistency
- [ ] CV follows the standard 2-page moderncv/banking format
- [ ] Cover letter uses cover.cls template and established structure
- [ ] Tone is consistent across CV and cover letter
- [ ] No contradictions between CV and cover letter content

### Quality
- [ ] No LaTeX syntax errors (balanced braces, correct commands)
- [ ] No spelling or grammar errors
- [ ] Agentic coding / AI tooling references mention **Antigravity** by name
- [ ] Cover letter is addressed to the correct person (or "Dear Hiring Manager" if unknown)
- [ ] Cover letter fits approximately one page

### Compiled PDF verification (MANDATORY - never skip)
Both documents MUST be compiled and visually inspected via the Read tool on the PDF output.
- [ ] CV compiled with **lualatex**. Cover letter compiled with **xelatex**.
- [ ] **CV is exactly 2 pages** - not 1, not 3
- [ ] **No orphaned `\cventry` titles** - use `\needspace{5\baselineskip}` before each `\cventry` to prevent this
- [ ] **Cover letter is exactly 1 page** - signature block must fit with the body, never overflow
- [ ] **Cover letter bullet font matches body font** - custom font configuration applied correctly
