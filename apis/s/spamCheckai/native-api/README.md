# SpamCheck.ai: Native API Reference

A consolidated summary of SpamCheck.ai's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://app.spamcheck.ai/api_docs/index.html
- **OpenAPI specification:** https://app.spamcheck.ai/swagger.yaml
- **API base URL:** `https://api.spamcheck.ai/api/v1`

## Authentication

### API Key

Authenticate SpamCheck.ai requests with the Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.spamcheck.ai/getting-started/)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Submission for Spam](actions/check-submission-for-spam.md) | `POST /spam/check` | [docs](https://app.spamcheck.ai/api_docs/index.html#/default/post_spam_check) |
| [Create Spam Report](actions/create-spam-report.md) | `POST /spam_reports` | [docs](https://app.spamcheck.ai/api_docs/index.html#/default/post_spam_reports) |
| [Delete Spam Report](actions/delete-spam-report.md) | `DELETE /spam_reports/:id` | [docs](https://app.spamcheck.ai/api_docs/index.html#/default/delete_spam_reports) |
| [List Spam Reports](actions/list-spam-reports.md) | `GET /spam_reports` | [docs](https://app.spamcheck.ai/api_docs/index.html#/default/get_spam_reports) |
