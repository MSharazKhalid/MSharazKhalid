<h1 align="center">Muhammad Sharaz Khalid</h1>

<p align="center">
  <b>Healthcare Automation Engineer</b> &nbsp;·&nbsp; Python &nbsp;·&nbsp; Full-Stack TypeScript &nbsp;·&nbsp; Data Engineering
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/sharaz-khalid-b50911239/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:sharazkhalid93@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/Lahore,_Pakistan-555?style=flat-square&logo=googlemaps&logoColor=white" alt="Location">
  <img src="https://img.shields.io/badge/Open_to-Freelance_&_Remote-2ea44f?style=flat-square" alt="Availability">
</p>

---

I build automation that removes manual work from regulated, high-volume workflows - and the web applications that put that automation in a client's hands.

Most of my work lives in US healthcare: extracting clinical data out of EHR platforms that were never designed to be queried, and turning CMS quality-measure rules into software that runs reliably against real patient data. The same engineering holds up outside healthcare - browser automation, document pipelines, and production SaaS - so I work across both.

Computer Science graduate of **UET Lahore**, with four years in healthcare data. Currently **Senior Data Analyst at DigiEvolve**, where I own the automation and MIPS reporting stack.

---

## What I do

<table>
<tr>
<td width="33%" valign="top">

### Healthcare Automation

Clinical data extraction across **13 EHR platforms** - Practice Fusion, NextGen, Epic, eClinicalWorks, Elation Health, AdvanceMD, DrChrono, ModMed, Tebra, PrognoCIS and PointClickCare.

MIPS quality-measure logic, ICD/CPT/POS normalisation, HCFA-1500 claim parsing, NPPES provider lookup.

</td>
<td width="33%" valign="top">

### Full-Stack Development

Production web apps end to end - **Fastify**, **Next.js 14**, **React**, **Flask**, **PostgreSQL**, **Supabase**, **Redis**, **BullMQ**.

Auth and RBAC, row-level security, background job queues, credit and billing systems, admin consoles, transactional email.

</td>
<td width="33%" valign="top">

### Data & Process Automation

Browser automation at scale with **Selenium** - session reuse, retry and resume, checkpointed progress, human-paced throttling.

Document and spreadsheet pipelines with **pandas**, **openpyxl**, **pdfplumber**, **PyMuPDF**, Google Sheets and Apps Script.

</td>
</tr>
</table>

---

## Tech stack

**Languages** &nbsp; Python · TypeScript · JavaScript · SQL · PHP · C

**Backend** &nbsp; Fastify · Flask · Node.js · Prisma · SQLAlchemy · REST APIs · BullMQ · Redis

**Frontend** &nbsp; Next.js 14 (App Router) · React 18 · Vite · Tailwind CSS · shadcn/ui · TanStack Query

**Data** &nbsp; PostgreSQL · MySQL · SQLite · Supabase · pandas · NumPy · openpyxl

**Automation** &nbsp; Selenium · BeautifulSoup · pdfplumber · PyMuPDF · pywin32 · Google Apps Script · Sheets API

**Infrastructure** &nbsp; Docker · Turborepo · Railway · Git · GitHub Actions

---

## Open-source tools

Focused, production-tested utilities pulled out of real engagements and cleaned up for public use.

| Tool | What it does | Stack |
|---|---|---|
| **[nppes-npi-scraper](https://github.com/MSharazKhalid/nppes-npi-scraper)** | Bulk-resolves NPI numbers against the CMS NPPES registry and writes each provider's primary practice address back into Excel | Python · Selenium · openpyxl |
| **[pdf-section-extractor](https://github.com/MSharazKhalid/pdf-section-extractor)** | Extracts text from a folder of PDFs by whole page, by named section, or below a section heading - with a bounding-box visualiser for calibrating coordinates | Python · pdfplumber · Pillow |
| **[pdf-keyword-search](https://github.com/MSharazKhalid/pdf-keyword-search)** | Finds any phrase, or every value in an Excel column, inside a PDF and reports the exact page of each hit | Python · PyMuPDF · openpyxl |
| **[ringcentral-fax-auto](https://github.com/MSharazKhalid/ringcentral-fax-auto)** | Drives the RingCentral web app to fax a PDF to every number in a Google Sheet, with human-like pacing and per-row status write-back | Python · Selenium · Sheets API |
| **[outlook-bulk-email](https://github.com/MSharazKhalid/outlook-bulk-email)** | Sends personalised HTML email to an Excel mailing list through desktop Outlook - rotates sender identities, batches sends, writes delivery status back | Python · pywin32 |
| **[measure-238-apps-script](https://github.com/MSharazKhalid/measure-238-apps-script)** | Flags MIPS Measure 238 high-risk medications by drug class, firing only when two or more same-class orders appear for a patient | Google Apps Script |
| **[excel-final-file-builder](https://github.com/MSharazKhalid/excel-final-file-builder)** | Turns a raw formatted Excel export into a clean, submission-ready workbook in a single run | Python · pandas · openpyxl |

---

## Client work

Built for clients and kept private. I am happy to walk through the architecture, the code and the decisions behind it on a call.

<table>
<tr><th align="left" width="26%">Project</th><th align="left">What it does</th></tr>

<tr><td valign="top"><b>EHR Automation Suite</b><br><sub>Python · Selenium</sub></td>
<td><b>94 automation scripts spanning 13 EHR platforms</b>, organised per platform and per CMS quality measure. Handles authenticated session reuse, retry-and-resume against flaky clinical UIs, checkpointed progress so a long run survives interruption, and incremental write-back so no extracted record is lost mid-run.</td></tr>

<tr><td valign="top"><b>IndexMeNow</b><br><sub>Fastify 5 · Next.js 14 · PostgreSQL · Redis</sub></td>
<td>Multi-tenant SaaS that accelerates Google indexing by firing <b>six indexing signals in parallel</b> per URL - Google Indexing API, GSC URL Inspection, sitemap ping, RSS/WebSub, IndexNow and crawl-trigger cache busting. A seven-point pre-flight health check means a credit is never spent on a bad URL, and a 10-day verification cycle refunds the credit automatically if the URL still is not indexed. Adds atomic credit accounting with Redis-cached balances, API-key access for programmatic submission, a WordPress auto-submit plugin, and an admin console over live BullMQ queue state. Turborepo monorepo with Dockerised Postgres and Redis.</td></tr>

<tr><td valign="top"><b>MIPS Denominator Engine</b><br><sub>Flask · React · pandas</sub></td>
<td>Web app that turns CMS quality-measure definitions into a reusable rule library. A four-step wizard takes the user from Excel upload through column mapping to processing and download. The engine evaluates <b>nested AND/OR/NOT logic plus patient-level predicates</b> - exclude-patient, patient-has, minimum-count - computes age at the anchor visit date rather than trusting a static column, and normalises messy real-world codes: ICD/CPT wildcard matching, dot stripping, Excel float artefacts (<code>95.0</code> → <code>95</code>) and restored leading zeros (<code>POS 2</code> → <code>02</code>). Covered by an engine test suite.</td></tr>

<tr><td valign="top"><b>Prime Well</b><br><sub>React · TypeScript · Supabase</sub></td>
<td>Role-separated clinical document platform with distinct admin and physician dashboards. Supabase Auth with <b>row-level security enforced in the database</b>, so a physician reaches only their own records and an admin only their assigned physicians. Includes a document upload and review workflow, private storage buckets with access policies, progress reporting, activity logs, in-app notifications and transactional email.</td></tr>

<tr><td valign="top"><b>Office Ally Billing Tools</b><br><sub>Python · pdfplumber</sub></td>
<td>Parses multi-page HCFA-1500 claim PDFs into one spreadsheet row per service line - patient demographics, Box 21 diagnosis codes, and Box 24 procedure codes with modifiers, charges, units and rendering provider. Paired with a chart-level ICD scraper that recycles its browser on a fixed interval and autosaves throughout, so long unattended runs finish cleanly.</td></tr>

</table>

---

## Experience

**Senior Data Analyst** - DigiEvolve &nbsp;·&nbsp; *April 2025 - Present*
**Data Analyst** - DigiEvolve &nbsp;·&nbsp; *October 2024 - March 2025*

- Own the automation and MIPS quality-reporting stack across a portfolio of US healthcare clients
- Build and maintain clinical data-extraction tooling spanning 13 EHR platforms
- Translate CMS quality-measure specifications into tested, reusable rule engines
- Develop internal web applications that put automation directly in client hands
- Lead a team of analysts and coordinate cross-functional data initiatives

**Data Specialist** - Sourcing Solutions &nbsp;·&nbsp; *June - November 2024*
&nbsp;&nbsp;Export data integrity and compliance reporting on SAP ERP.

**Data Operations Specialist → Growth Associate** - Healthwire &nbsp;·&nbsp; *August 2022 - May 2024*
&nbsp;&nbsp;Healthcare platform. Started in data verification and reporting, then moved to user behaviour analysis, A/B testing and retention campaigns.

**Freelance - B2B Data Extraction** &nbsp;·&nbsp; *July 2020 - August 2022*
&nbsp;&nbsp;Lead sourcing and data enrichment for sales teams, delivered through Fiverr.

---

## Education

**BSc Computer Science** - University of Engineering and Technology (UET), Lahore &nbsp;·&nbsp; *2020 - 2024*

---

## GitHub

<p align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=MSharazKhalid&show_icons=true&include_all_commits=true&count_private=true&hide_border=true&title_color=0A66C2&icon_color=0A66C2&hide=issues" alt="GitHub stats">
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=MSharazKhalid&layout=compact&hide_border=true&title_color=0A66C2&langs_count=8" alt="Top languages">
</p>

---

## Work with me

I take on automation and full-stack work, both freelance and long-term remote. I am most useful where a workflow is **repetitive, high-volume and expensive to get wrong** - clinical data extraction, regulatory reporting, document pipelines, or an internal tool replacing a spreadsheet nobody trusts any more.

If a project above is private, just ask and I will walk you through it.

<p align="left">
  <a href="mailto:sharazkhalid93@gmail.com"><img src="https://img.shields.io/badge/sharazkhalid93@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  &nbsp;
  <a href="https://www.linkedin.com/in/sharaz-khalid-b50911239/"><img src="https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
</p>
