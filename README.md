# SYSTRAN (systran)

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
