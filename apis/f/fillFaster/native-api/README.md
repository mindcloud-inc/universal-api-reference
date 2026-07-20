# FillFaster: Native API Reference

A consolidated summary of FillFaster's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ
- **API base URL:** `https://api.fillfaster.com`

## Authentication

### API Key

Use a FillFaster API token from https://fillfaster.com/account/develop/

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://fillfaster.com/account/develop)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bulk Submissions](actions/create-bulk-submissions.md) | `POST /v1/submission/createBulkSubmissions` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#7df8f71d-2da7-4e4b-bc71-6300c6916d14) |
| [Create Submission Link](actions/create-submission-link.md) | `POST /v1/createSubmission` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#a9ea4e58-0474-45e3-ba68-3e46b387fb9d) |
| [Generate PDF](actions/generate-pdf.md) | `POST /v1/generatePDF` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#f726d97c-c44c-4b68-86a7-7f06bb1db8c2) |
| [Get Form Fields](actions/get-form-fields.md) | `POST /v1/getFormFields` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#896e6612-7996-4865-8a84-12f012e74774) |
| [Get Form Settings](actions/get-form-settings.md) | `GET /v1/form/:formId/settings` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#af7f3880-3f36-4bcf-b5a6-fd92e546006a) |
| [Get Submission PDF](actions/get-submission-pdf.md) | `GET /v1/getSubmissionPDF/:submissionId` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#2e94561c-78c4-4d02-95ef-f52fc554e898) |
| [Get Submission Status](actions/get-submission-status.md) | `GET /v1/getSubmissionStatus/:submissionId` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#b66ea34b-0a2d-4d0c-ac18-1a17f6300d44) |
| [Get Submissions List](actions/get-submissions-list.md) | `GET /v1/getSubmissionsList` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#480d33e7-835e-4236-bcdc-abef6a23cad1) |
| [List Forms](actions/list-forms.md) | `GET /v1/getFormsList` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ) |
| [Subscribe Webhook](actions/subscribe-webhook.md) | `POST /v1/form/:formId/webhook/subscribe` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#115ff600-bfc7-4954-ac9e-b79402abba71) |
| [Unsubscribe Webhook](actions/unsubscribe-webhook.md) | `POST /v1/form/:formId/webhook/unsubscribe` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#0ec7d0f3-0bc0-4723-9816-00153a6a9e85) |
| [Update Form Settings](actions/update-form-settings.md) | `POST /v1/form/update-settings` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ) |
| [Update Submission](actions/update-submission.md) | `POST /v1/submission/update` | [docs](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#24a91702-5d18-436b-bdc0-4c5d77f2953d) |
