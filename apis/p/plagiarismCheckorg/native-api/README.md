# PlagiarismCheck.org: Native API Reference

A consolidated summary of PlagiarismCheck.org's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://plagiarismcheck.org/for-developers/
- **API base URL:** `https://plagiarismcheck.org`

## Authentication

### API Key

Authenticate with a PlagiarismCheck.org personal API token sent in the X-API-TOKEN header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-TOKEN: <apiKey>
```

[Official authentication documentation](https://plagiarismcheck.org/for-developers/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Organization Check](actions/delete-organization-check.md) | `POST /api/org/text/delete/:id/` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Get AI Check Report](actions/get-ai-check-report.md) | `GET /api/v1/chat-gpt/:id` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Get AI Check Status](actions/get-ai-check-status.md) | `GET /api/v1/chat-gpt/:id` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Get Organization Check Status](actions/get-organization-check-status.md) | `POST /api/org/text/status/:id/` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Get Organization Report](actions/get-organization-report.md) | `POST /api/org/text/report/:id/` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Get Plagiarism Check Status](actions/get-plagiarism-check-status.md) | `GET /api/v1/text/:id` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Get Plagiarism Report](actions/get-plagiarism-report.md) | `GET /api/v1/text/report/:id` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Submit AI Check For B2B Group](actions/submit-ai-check-for-b2b-group.md) | `POST /api/v1/chat-gpt/` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Submit AI Check From File](actions/submit-ai-check-from-file.md) | `POST /api/v1/chat-gpt/` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Submit AI Check From Text](actions/submit-ai-check-from-text.md) | `POST /api/v1/chat-gpt/` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Submit Organization Check With Custom Author](actions/submit-organization-check-with-custom-author.md) | `POST /api/org/text/check/` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Submit Organization File Check](actions/submit-organization-file-check.md) | `POST /api/org/text/check/` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Submit Organization Plagiarism Check](actions/submit-organization-plagiarism-check.md) | `POST /api/org/text/check/` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Submit Plagiarism Check](actions/submit-plagiarism-check.md) | `POST /api/v1/text` | [docs](https://plagiarismcheck.org/for-developers/) |
| [Validate Plagiarism Text Before Submit](actions/validate-plagiarism-text-before-submit.md) | `POST /api/v1/text/validate` | [docs](https://plagiarismcheck.org/for-developers/) |
