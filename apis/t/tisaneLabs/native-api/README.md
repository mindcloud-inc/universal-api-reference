# Tisane Labs: Native API Reference

A consolidated summary of Tisane Labs's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.tisane.ai/apis/tisane-api-short
- **OpenAPI specification:** https://docs.tisane.ai/_bundle/apis/tisane-api-short.json?download=
- **API base URL:** `https://api.tisane.ai`

## Authentication

### Tisane API Key

Authenticate Tisane API requests with an API subscription key sent in the Ocp-Apim-Subscription-Key header.

### Credentials

- **API Key:** `apiKey` · required · Raw Tisane API subscription key. This value is sent as the Ocp-Apim-Subscription-Key header.

Send these headers with each API request:

```http
Ocp-Apim-Subscription-Key: <apiKey>
```

[Official authentication documentation](https://docs.tisane.ai/quickstart/quickstart)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Text](actions/analyze-text.md) | `POST /parse` | [docs](https://docs.tisane.ai/apis/tisane-api-short#tag/NLU-/-NLP-Methods/operation/parse) |
| [Compare Entities](actions/compare-entities.md) | `POST /compare/entities` | [docs](https://docs.tisane.ai/apis/tisane-api-short#tag/NLU-/-NLP-Methods/operation/compareEntities) |
| [Detect Language](actions/detect-language.md) | `POST /detectLanguage` | [docs](https://docs.tisane.ai/apis/tisane-api-short#tag/NLU-/-NLP-Methods/operation/detectLanguage) |
| [Extract Text](actions/extract-text.md) | `POST /helper/extract_text` | [docs](https://docs.tisane.ai/apis/tisane-api-short#tag/NLU-/-NLP-Methods/operation/extract_text) |
| [List Inflected Forms](actions/list-inflected-forms.md) | `GET /lm/inflections` | [docs](https://docs.tisane.ai/apis/tisane-api-short#tag/Language-Model-Direct-Access/operation/inflections) |
| [List Languages](actions/list-languages.md) | `GET /languages` | [docs](https://docs.tisane.ai/apis/tisane-api-short#tag/NLU-/-NLP-Methods/operation/languages) |
| [Translate Text](actions/translate-text.md) | `POST /transform` | [docs](https://docs.tisane.ai/apis/tisane-api-short#tag/NLU-/-NLP-Methods/operation/transform) |
