# AI21 Labs: Native API Reference

A consolidated summary of AI21 Labs's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.ai21.com/reference/introduction
- **API base URL:** `https://api.ai21.com/studio/v1`

## Authentication

### API Key

Authenticate AI21 API requests with a bearer API key from AI21 Studio.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ai21.com/reference/authentication)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Sentiment](actions/analyze-sentiment.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Brainstorm Ideas](actions/brainstorm-ideas.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Classify Text](actions/classify-text.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Compare Texts](actions/compare-texts.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Convert To Bullet List](actions/convert-to-bullet-list.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Convert To JSON](actions/convert-to-json.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Create Executive Brief](actions/create-executive-brief.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Create Maestro Run](actions/create-maestro-run.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Create Outline](actions/create-outline.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Draft Email](actions/draft-email.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Draft Meeting Notes](actions/draft-meeting-notes.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Evaluate Against Requirements](actions/evaluate-against-requirements.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Explain Technical Concept](actions/explain-technical-concept.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Extract Keywords](actions/extract-keywords.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Extract Structured Data](actions/extract-structured-data.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Generate Action Items](actions/generate-action-items.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Generate Blog Draft](actions/generate-blog-draft.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Generate Checklist](actions/generate-checklist.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Generate FAQ](actions/generate-faq.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Generate Product Description](actions/generate-product-description.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Generate Social Post](actions/generate-social-post.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Generate Study Guide](actions/generate-study-guide.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Identify Risks](actions/identify-risks.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [List Library Files](actions/list-library-files.md) | `GET /library/files` | [docs](https://docs.ai21.com/reference/manage-library-ref/list-library-files) |
| [Retrieve Maestro Run](actions/retrieve-maestro-run.md) | `GET /maestro/runs/:run_id` | [docs](https://docs.ai21.com/reference/retrieve-run) |
| [Review Document](actions/review-document.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Rewrite Text](actions/rewrite-text.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Simplify Text](actions/simplify-text.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Summarize Text](actions/summarize-text.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
| [Translate Text](actions/translate-text.md) | `POST /maestro/runs` | [docs](https://docs.ai21.com/reference/maestro-create-run) |
