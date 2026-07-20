# <img src="https://images.mindcloud.co/apps/icons/rosette-icon_1776196677133.jpeg" alt="Rosette Text Analytics logo" width="28" height="28"> Rosette Text Analytics: Universal API

Analyze text with Rosette endpoints for language detection, tokenization, entity extraction, sentiment, topics, semantic vectors, and identity matching.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rosetteTextAnalytics/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.babelstreet.com
- **Vendor API docs:** https://docs.babelstreet.com/en/index-en.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check API Status](actions/check-api-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/check-api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Morphology](actions/analyze-morphology.md) | GET |  |
| [Analyze Sentiment](actions/analyze-sentiment.md) | GET |  |
| [Check API Status](actions/check-api-status.md) | GET |  |
| [Compare Address Similarity](actions/compare-address-similarity.md) | GET |  |
| [Compare Name Similarity](actions/compare-name-similarity.md) | GET |  |
| [Deduplicate Names](actions/deduplicate-names.md) | GET |  |
| [Extract Entities](actions/extract-entities.md) | GET |  |
| [Extract Topics](actions/extract-topics.md) | GET |  |
| [Find Semantically Similar Terms](actions/find-semantically-similar-terms.md) | GET |  |
| [Generate Semantic Vector](actions/generate-semantic-vector.md) | GET |  |
| [Get API Information](actions/get-api-information.md) | GET |  |
| [Identify Language](actions/identify-language.md) | GET |  |
| [List Address Similarity Languages](actions/list-address-similarity-languages.md) | GET |  |
| [List Entity Extraction Languages](actions/list-entity-extraction-languages.md) | GET |  |
| [List Language Identification Languages](actions/list-language-identification-languages.md) | GET |  |
| [List Morphology Languages](actions/list-morphology-languages.md) | GET |  |
| [List Name Deduplication Languages](actions/list-name-deduplication-languages.md) | GET |  |
| [List Name Similarity Languages](actions/list-name-similarity-languages.md) | GET |  |
| [List Name Translation Languages](actions/list-name-translation-languages.md) | GET |  |
| [List Sentence Splitting Languages](actions/list-sentence-splitting-languages.md) | GET |  |
| [List Tokenization Languages](actions/list-tokenization-languages.md) | GET |  |
| [Split Sentences](actions/split-sentences.md) | GET |  |
| [Tokenize Text](actions/tokenize-text.md) | GET |  |
| [Translate Name](actions/translate-name.md) | GET |  |

