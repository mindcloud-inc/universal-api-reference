# Rosette Text Analytics: Native API Reference

A consolidated summary of Rosette Text Analytics's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.babelstreet.com/en/index-en.html
- **API base URL:** `https://api.rosette.com/rest/v1`

## Authentication

### API Key

Hosted Rosette Cloud API key sent in the X-RosetteAPI-Key request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-rosetteapi-key: <apiKey>
```

[Official authentication documentation](https://docs.babelstreet.com/en/index-en.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |
| `content-type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,503`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Morphology](actions/analyze-morphology.md) | `POST /morphology/:morphoFeature` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Analyze Sentiment](actions/analyze-sentiment.md) | `POST /sentiment` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Check API Status](actions/check-api-status.md) | `GET /ping` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Compare Address Similarity](actions/compare-address-similarity.md) | `POST /address-similarity` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Compare Name Similarity](actions/compare-name-similarity.md) | `POST /name-similarity` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Deduplicate Names](actions/deduplicate-names.md) | `POST /name-deduplication` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Extract Entities](actions/extract-entities.md) | `POST /entities` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Extract Topics](actions/extract-topics.md) | `POST /topics` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Find Semantically Similar Terms](actions/find-semantically-similar-terms.md) | `POST /semantics/similar` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Generate Semantic Vector](actions/generate-semantic-vector.md) | `POST /semantics/vector` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Get API Information](actions/get-api-information.md) | `GET /info` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Identify Language](actions/identify-language.md) | `POST /language` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [List Address Similarity Languages](actions/list-address-similarity-languages.md) | `GET /address-similarity/supported-languages` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [List Entity Extraction Languages](actions/list-entity-extraction-languages.md) | `GET /entities/supported-languages` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [List Language Identification Languages](actions/list-language-identification-languages.md) | `GET /language/supported-languages` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [List Morphology Languages](actions/list-morphology-languages.md) | `GET /morphology/supported-languages` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [List Name Deduplication Languages](actions/list-name-deduplication-languages.md) | `GET /name-deduplication/supported-languages` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [List Name Similarity Languages](actions/list-name-similarity-languages.md) | `GET /name-similarity/supported-languages` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [List Name Translation Languages](actions/list-name-translation-languages.md) | `GET /name-translation/supported-languages` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [List Sentence Splitting Languages](actions/list-sentence-splitting-languages.md) | `GET /sentences/supported-languages` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [List Tokenization Languages](actions/list-tokenization-languages.md) | `GET /tokens/supported-languages` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Split Sentences](actions/split-sentences.md) | `POST /sentences` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Tokenize Text](actions/tokenize-text.md) | `POST /tokens` | [docs](https://docs.babelstreet.com/en/index-en.html) |
| [Translate Name](actions/translate-name.md) | `POST /name-translation` | [docs](https://docs.babelstreet.com/en/index-en.html) |
