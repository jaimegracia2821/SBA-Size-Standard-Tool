 # NAICS Size Standard Impact Tool

Find the federal contractors whose small-business status would change when an SBA size
standard moves — and draft a comment to SBA about it.

**[Open the tool →](https://jaimegracia2821.github.io/SBA-Size-Standard-Tool/)**

Runs entirely in your browser. No account, no sign-in, no installation. Your data is never
uploaded anywhere.

---

## What it does

When SBA changes a size standard, some firms that are too large to count as small today
become small, and a smaller number move the other way. This tool identifies the firms whose
status would change, using public federal contract data, and shows how each of them competes
today.

Give it a spending extract from USAspending.gov and two dollar thresholds. It returns:

- **The cohort** — every parent company whose federal obligations fall between the current and
  proposed standards, with a five-year average matching the averaging period at 13 CFR 121.104
- **How they win work** — the split between full and open competition and each category of
  set-aside, per company per fiscal year
- **A confidence rating per company**, flagging where the estimate is least reliable
- **A verification checklist** for signing off on figures before you publish them
- **A draft comment to SBA**, built from your own numbers

It works on any NAICS code and any pair of thresholds. It ships pre-loaded for the August 2026
proposed rule affecting management consulting (Docket SBA-2026-0199), but nothing about the
analysis is specific to that rule.

---

## Read this before you use the output

**The tool measures federal prime contract dollars. Size standards measure total company
receipts.**

Under 13 CFR 121.104, size is based on average annual receipts over five fiscal years, from
every revenue source, with affiliates included. Commercial revenue, subcontract revenue, and
affiliate revenue do not appear in federal award data at all.

A company can therefore look small in this output and be well over the threshold in fact. What
you get is a **ranked list of candidates worth investigating** — not a determination of who is
small, and it should never be presented as one. Size determinations rest with SBA and the
contracting officer.

The tool flags this in its own output, and rates each company by how reliable its estimate is.
The largest firms in any cohort are usually the least reliable, because they carry the most
revenue this data cannot see.

---

## Getting started

1. **Download the data.** On [USAspending.gov](https://www.usaspending.gov), go to Award Search
   → Advanced Search → Download → Custom Award Data. Choose **Contracts** and **Prime Award
   Transactions** — not the award summaries. Filter to your NAICS codes and set the date range
   to five full federal fiscal years (October 1 to September 30).

2. **Open the tool** and drop in the ZIP. Don't unpack it; the tool finds the right file.

3. **Confirm the scope and thresholds**, then run it.

The tool will not guess a size standard it doesn't have. Codes that look closely related often
carry different standards — within the management consulting group alone the current figures
range from $19.0M to $29.0M — and a wrong threshold produces a plausible-looking list of the
wrong companies. Every standard loaded into the tool must carry a stated source.

Full instructions are in the [User Guide](TWG_Size_Standard_Tool_User_Guide.docx).

---

## Commenting on a proposed rule

Agencies must respond to significant comments. Sentiment is not significant; a position backed
by data is.

The tool drafts a comment around the figures from your run and outputs an **unbranded Word
document** — no header, no footer, no styling — that pastes cleanly into your own letterhead.

**The tool takes no position on the rule.** The analysis measures; it does not argue. You choose
your position — oppose the increase, support it, support it with modifications, or take no
position and submit the data alone — and the argument sections are written to whichever you
pick. The section reporting what the award record shows is identical under every position,
because the measurement doesn't change with your view of it.

Two things the tool does to protect the filing:

- It scans the draft and flags any number that doesn't trace back to your authorized figures.
  One unsupported figure gets an entire comment discounted.
- It tells you which sections to rewrite in your own words. Sections arguing from the
  rulemaking record will read alike across filers, and agencies discount identical submissions
  as a form campaign.

**Comments on Docket SBA-2026-0199 close September 21, 2026.** Check
[regulations.gov](https://www.regulations.gov) for current status.

---

## Privacy

Your file is read inside your browser and nothing is transmitted anywhere. There is no server,
no analytics, and no logging. That means the tool can be used with sensitive pipeline data, and
it means nobody but you holds a copy of what you analyzed. Closing the tab discards everything.

You can also download `index.html` and open it from your own disk — it works offline apart from
three libraries it loads from a CDN.

---

## Known limitations

- Employee-based size standards cannot be analyzed; spending data contains no headcount
- Subcontract revenue is absent, understating firms that work largely as subcontractors
- Obligations are recorded at award while revenue is earned over the performance period, so
  annual figures are lumpier than actual revenue
- Company identification depends on the parent identifier in the source data, which is
  incomplete, and on name matching, which is imperfect — every merge is logged for review
- Very large files are limited by your computer's memory; use a desktop browser

---

## Built with

[SheetJS Community Edition](https://sheetjs.com) (Apache-2.0) and
[JSZip](https://stuk.github.io/jszip/). Word documents are generated directly as Office Open
XML with no additional dependency.

---

## Copyright and terms

Copyright © 2026 The Wolverine Group, Inc. All rights reserved.

Provided free of charge for use in analyzing and commenting on SBA Docket SBA-2026-0199 and the
companion methodology docket SBA-2026-0265.

---

## Disclaimer

This tool is provided by The Wolverine Group, Inc. for general informational and educational
purposes only. It reflects business and practitioner guidance, not legal, financial, or tax
advice, and does not create an attorney-client, advisory, or fiduciary relationship of any kind.

The tool produces estimates derived from public federal spending data. It does not and cannot
determine any firm's size status under the Small Business Act or 13 CFR Part 121, and its output
is not a size determination, a size certification, or a substitute for either. Size standards,
size determinations, affiliation, and eligibility rest with the U.S. Small Business
Administration and the contracting officer, and turn on facts not present in this data.

Proposed rules are subject to change or withdrawal and confer no rights. Nothing here should be
read as a recommendation to alter a size representation, certification, teaming arrangement, or
bid strategy. Verify every threshold and citation against primary sources, and have any
regulatory submission or business decision reviewed by qualified legal counsel, and where
appropriate a financial or tax professional, before acting.

The Wolverine Group, Inc. makes no representations or warranties as to the accuracy,
completeness, or suitability of this material for your situation, and disclaims, to the fullest
extent permitted by law, any liability for decisions made or actions taken in reliance on it.
You remain solely responsible for your own business decisions.
