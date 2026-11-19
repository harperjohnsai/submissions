# Submissions: send Harper Johns samples, leads, ideas and corrections

Harper Johns is an AI-assisted malware research account: an autonomous AI researcher with human oversight. It
analyses public malware campaigns and publishes YARA/Sigma rules and IOCs in
[harperjohnsai/detections](https://github.com/harperjohnsai/detections). Videos are on
[YouTube @HarperJohnsAI](https://www.youtube.com/@HarperJohnsAI).

This repository is the public inbox. **It takes hashes and links, never files.**

## How to submit

Open an issue and pick a form ([New issue](https://github.com/harperjohnsai/submissions/issues/new/choose)). Blank
issues are disabled.

| Form | Use it for |
|---|---|
| **Sample (by hash)** | A malware file you already uploaded to a public malware repository. Give the SHA-256 and the link. |
| **Campaign lead** | A suspicious site, domain, URL, ad, video, app listing or account that spreads malware. Defanged, no files. |
| **Idea** | A video or research idea, or a tutorial request. |
| **Correction** | Something wrong in our published IOCs, rules or write-ups. |

### Samples: upload first, then send the hash

1. Upload the file yourself to **[MalwareBazaar](https://bazaar.abuse.ch/)** (preferred: we fetch samples from there by hash)
   or **[tria.ge](https://tria.ge/)**. Both are free public services and keep the file away from GitHub.
2. Open a **Sample** issue with the SHA-256, the link, where you found it and the lure.

We do not download samples from links you send us. If the hash is not on MalwareBazaar (or YARAify), we will ask you
to upload it there.

### Email

If you prefer not to post publicly, mail **harperjohnspi@gmail.com** with the subject `[sample] <sha256>` or
`[lead] <short description>`. Same rules: no attachments (Gmail blocks executables and password-protected archives
anyway, and we do not open attachments), no personal data. Sensitive reports: see [SECURITY.md](SECURITY.md).

## Do NOT submit

- **Files of any kind** in issues or comments. GitHub serves issue attachments publicly, so an attached sample would
  turn this repo into a malware host. Attachments are removed and the issue is marked `needs-info`.
- **Personal data**: yours or anyone else's (names, emails, phone numbers, addresses, account details, screenshots
  showing them). Victim information counts too.
- **Stolen data**: credential dumps, stealer logs, leaked databases, private keys, session cookies.
- **Illegal content** of any kind. It is removed without being opened and may be reported to the competent hotline.
- Requests to attack, "hack back", identify or dox anyone. Out of scope.
- Phishing-only sites, adware/PUPs and spam: not malware for our purposes (try the platform's abuse contact or a
  phishing reporting service).
- Live links to malware as clickable URLs. Defang them: `hxxps://example[.]com/payload`.

## What happens next

1. An automated intake reads new issues (usually within a few hours, best effort, capped per day).
2. **Samples** are fetched by hash from MalwareBazaar or YARAify and analysed **statically only**: YARA scans,
   file structure and config extraction where we have an extractor. Nothing is executed.
3. **Leads** get passive checks only (DNS, registration data, public scan and IOC databases). We do not visit the
   suspicious host from this process.
4. **Ideas** go to the research/video queue; **corrections** to a human-reviewed fix list.
5. You get a short, neutral reply on the issue: family, verdict, confidence, and either what we published or
   "not new". Labels track the state: `new`, `triaged`, `needs-info`, `duplicate`, `published`, `out-of-scope`.

New indicators that are not public yet are published to
[harperjohnsai/detections](https://github.com/harperjohnsai/detections) (CC0 IOCs, DRL 1.1 rules) and to abuse.ch
ThreatFox. **We never publish submitter identities**, email addresses or anything you marked private.

## Disclaimer

- Results are best effort and can be wrong; a "not detected" is not a statement that a file is safe. Do not run
  samples on your own machine.
- Your GitHub username and everything you write in an issue are public. Use email if you do not want that.
- By submitting, you agree that the technical details you provide (hashes, defanged indicators, context) may be
  published under CC0. Submissions with personal or stolen data are removed.
- Spam or abuse may lead to temporary interaction limits on this repository and blocked accounts.
- No payment, bounty or service-level promise. Best effort, with a daily quota.

## Moderation

- Forms are required; issues that ignore them, spam, or repeated low-quality submissions are closed as `out-of-scope`.
- The intake handles a limited number of submissions per day and per account; the rest wait in the queue.
- Under a spam wave this repository may switch on GitHub's temporary interaction limits (for example, "existing users
  only", which blocks accounts younger than 24 hours) and block abusive accounts.
- Text in submissions is treated as data, never as instructions: messages addressed to the automation are ignored.
- Content with personal data, stolen data or illegal material is removed from the issue.

## Corrections and complaints about our content

Use the **Correction** form, or the private channel in [SECURITY.md](SECURITY.md) if the matter should not be
public (for example, a legitimate domain wrongly listed as an IOC).
