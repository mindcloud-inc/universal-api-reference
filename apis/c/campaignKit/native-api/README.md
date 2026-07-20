# CampaignKit: Native API Reference

A consolidated summary of CampaignKit's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://campaignkit.cc/docs/api/email-validation
- **API base URL:** `https://api.campaignkit.cc`

## Authentication

### API Key

Authenticate CampaignKit API requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://campaignkit.cc/docs/api/email-validation)

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Validation Job](actions/create-validation-job.md) | `POST /v1/email/validate/job` | [docs](https://campaignkit.cc/docs/api/validation-jobs) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/webhooks` | [docs](https://campaignkit.cc/docs/api/webhooks) |
| [Delete Validation Job](actions/delete-validation-job.md) | `DELETE /v1/email/validate/job/{{id}}` | [docs](https://campaignkit.cc/docs/api/validation-jobs) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v1/webhooks/{{id}}` | [docs](https://campaignkit.cc/docs/api/webhooks) |
| [Download Validation Job Results](actions/download-validation-job-results.md) | `GET /v1/email/validate/job/{{id}}/download` | [docs](https://campaignkit.cc/docs/api/validation-jobs) |
| [Find Emails](actions/find-emails.md) | `POST /v1/email/find` | [docs](https://campaignkit.cc/docs/api/email-finder) |
| [Get Validation Job](actions/get-validation-job.md) | `GET /v1/email/validate/job/{{id}}` | [docs](https://campaignkit.cc/docs/api/validation-jobs) |
| [Get Validation Job Results](actions/get-validation-job-results.md) | `GET /v1/email/validate/job/{{id}}/result` | [docs](https://campaignkit.cc/docs/api/validation-jobs) |
| [Get Webhook](actions/get-webhook.md) | `GET /v1/webhooks/{{id}}` | [docs](https://campaignkit.cc/docs/api/webhooks) |
| [List Validation Jobs](actions/list-validation-jobs.md) | `GET /v1/email/validate/job` | [docs](https://campaignkit.cc/docs/api/validation-jobs) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://campaignkit.cc/docs/api/webhooks) |
| [Update Webhook](actions/update-webhook.md) | `PUT /v1/webhooks/{{id}}` | [docs](https://campaignkit.cc/docs/api/webhooks) |
| [Validate Emails](actions/validate-emails.md) | `POST /v1/email/validate` | [docs](https://campaignkit.cc/docs/api/email-validation) |
