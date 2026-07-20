# Winston AI: Native API Reference

A consolidated summary of Winston AI's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://docs.gowinston.ai/api-reference/introduction
- **API base URL:** `https://api.gowinston.ai`

## Authentication

### API Key

Use a Winston AI developer token from dev.gowinston.ai.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.gowinston.ai/api-reference/introduction)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Facts](actions/check-facts.md) | `POST /v2/fact-checker` | [docs](https://docs.gowinston.ai/api-reference/v2/fact-checker/post) |
| [Check Plagiarism](actions/check-plagiarism.md) | `POST /v2/plagiarism` | [docs](https://docs.gowinston.ai/api-reference/v2/plagiarism/post) |
| [Compare Text](actions/compare-text.md) | `POST /v2/text-compare` | [docs](https://docs.gowinston.ai/api-reference/v2/text-compare/post) |
| [Detect AI Image](actions/detect-ai-image.md) | `POST /v2/image-detection` | [docs](https://docs.gowinston.ai/api-reference/v2/image-detection/post) |
| [Detect AI Text](actions/detect-ai-text.md) | `POST /v2/ai-content-detection` | [docs](https://docs.gowinston.ai/api-reference/v2/ai-content-detection/post) |
