# <img src="https://images.mindcloud.co/apps/icons/tisane-labs-icon_1776699184091.png" alt="Tisane Labs logo" width="28" height="28"> Tisane Labs: Universal API

Tisane Labs provides multilingual text analysis, content moderation, language detection, semantic similarity, translation, and language model lookup APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tisaneLabs/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tisane.ai
- **Vendor API docs:** https://docs.tisane.ai/apis/tisane-api-short

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Languages](actions/list-languages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/list-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Detected Language

| Action | Method | Description |
| --- | --- | --- |
| [Detect Language](actions/detect-language.md) | GET | Detects input language in Tisane Labs. |

### Entity Comparison

| Action | Method | Description |
| --- | --- | --- |
| [Compare Entities](actions/compare-entities.md) | GET | Compares named entities in Tisane Labs. |

### Extracted Text

| Action | Method | Description |
| --- | --- | --- |
| [Extract Text](actions/extract-text.md) | GET | Extracts plain text from HTML in Tisane Labs. |

### Inflection

| Action | Method | Description |
| --- | --- | --- |
| [List Inflected Forms](actions/list-inflected-forms.md) | GET | Retrieves inflected forms from Tisane Labs. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Languages](actions/list-languages.md) | GET | Retrieves supported languages from Tisane Labs. |

### Text Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Text](actions/analyze-text.md) | GET | Analyzes input text in Tisane Labs. |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [Translate Text](actions/translate-text.md) | GET | Translates input text in Tisane Labs. |

