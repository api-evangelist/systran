# SYSTRAN (systran)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

SYSTRAN is a machine translation and natural language processing company offering neural (Pure Neural Machine Translation / PNMT) translation across 50+ languages. The SYSTRAN Translate API is a RESTful service (base `https://api-translate.systran.net`) that translates text, files, and HTML, detects and lists supported languages, and manages translation profiles, user dictionaries, and corpora. The broader SYSTRAN Platform / SYSTRAN.io surface adds NLP operations - morphology, tokenization, segmentation, named entity recognition, and language identification. Requests authenticate with an API key (the `key` query parameter or an `Authorization` header). SYSTRAN sells access as a Developer cloud subscription (14-day / 500,000-character free trial) plus Professional SaaS and Enterprise cloud/on-premise plans, billed per character.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/systran/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/systran/refs/heads/main/apis.yml)

## Tags

- Machine Translation
- Translation
- NLP
- Neural Machine Translation
- Localization
- Language Detection

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### SYSTRAN Translation API

Translate text and inline HTML from a source language to a target language with SYSTRAN Pure Neural Machine Translation. Supports profile selection, format handling, and translation feedback via `POST /translation/text/translate` and the supportedFormats / supportedSelectors / apiVersion utility endpoints.

- **Human URL:** [https://docs.systran.net/translateAPI/translation/](https://docs.systran.net/translateAPI/translation/)
- **Base URL:** `https://api-translate.systran.net`

### SYSTRAN File Translation API

Submit documents for asynchronous translation and manage translation jobs and batches - `POST /translation/file/translate` (with `async=true`), poll `GET /translation/file/status` by `requestId`, retrieve `GET /translation/file/result`, and create/close/cancel batches under `/translation/file/batch`.

- **Human URL:** [https://docs.systran.net/translateAPI/translation/](https://docs.systran.net/translateAPI/translation/)
- **Base URL:** `https://api-translate.systran.net`

### SYSTRAN Supported Languages API

Discover which language pairs, model options, formats, and selectors (domains, owners, sizes) are available - `GET /translation/supportedLanguages`, `GET /translation/supportedFeatures`, `GET /translation/supportedFormats`, and `GET /translation/supportedSelectors`.

- **Human URL:** [https://docs.systran.net/translateAPI/translation/](https://docs.systran.net/translateAPI/translation/)
- **Base URL:** `https://api-translate.systran.net`

### SYSTRAN Language Detection API

Automatically identify the language of a piece of text through the SYSTRAN.io / Platform NLP language-identification service (`GET /nlp/lid/detectLanguage`) and list the languages it can recognize (`GET /nlp/lid/supportedLanguages`).

- **Human URL:** [https://help.systrangroup.com/hc/en-us/sections/360004529440--REST-API](https://help.systrangroup.com/hc/en-us/sections/360004529440--REST-API)
- **Base URL:** `https://api-platform.systran.net`

### SYSTRAN NLP API

Natural language processing over the SYSTRAN.io / Platform NLP surface - morphological analysis (`GET /nlp/morphology/extractRoots`), tokenization (`GET /nlp/tokenization/tokenize`), segmentation (`GET /nlp/segmentation/segment`), and named entity recognition (`GET /nlp/ner/extractNamedEntities`).

- **Human URL:** [https://help.systrangroup.com/hc/en-us/sections/360004529440--REST-API](https://help.systrangroup.com/hc/en-us/sections/360004529440--REST-API)
- **Base URL:** `https://api-platform.systran.net`

### SYSTRAN Dictionary API

Look up multilingual dictionary entries and manage user dictionaries and their entries - `GET /resources/dictionary/lookup` plus create, update, delete, list, import, export, and apply operations under `/resources/dictionary`.

- **Human URL:** [https://docs.systran.net/translateAPI/dictionary/](https://docs.systran.net/translateAPI/dictionary/)
- **Base URL:** `https://api-translate.systran.net`

### SYSTRAN Profiles API

Create and manage translation profiles that bundle a language pair with dictionaries, corpora, and model options, and control their permissions - `GET /profiles`, `POST /profiles/create`, activate/deactivate/delete, and `GET/POST /profiles/{id}/permissions`, plus `GET /translationResources`.

- **Human URL:** [https://docs.systran.net/translateAPI/profiles/](https://docs.systran.net/translateAPI/profiles/)
- **Base URL:** `https://api-translate.systran.net`

### SYSTRAN Corpus API

Manage translation-memory corpora and their bilingual segments - add, import, list, export, match, update, and delete corpora under `/resources/corpus`, plus segment and segment-target CRUD used to adapt and tune translation output.

- **Human URL:** [https://docs.systran.net/translateAPI/corpus/](https://docs.systran.net/translateAPI/corpus/)
- **Base URL:** `https://api-translate.systran.net`

## Common Properties

- [GitHub Organization](https://github.com/SYSTRAN)
- [LinkedIn](https://www.linkedin.com/company/systran)
- [Website](https://www.systran.net)
- [Documentation](https://docs.systran.net/translateAPI/en/)
- [Plans](plans/systran-plans-pricing.yml)
- [Rate Limits](rate-limits/systran-rate-limits.yml)
- [Fin Ops](finops/systran-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
