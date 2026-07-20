# EmailListVerify: Native API Reference

A consolidated summary of EmailListVerify's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://api.emaillistverify.com/api-doc
- **OpenAPI specification:** https://api.emaillistverify.com/api-doc-json
- **API base URL:** `https://api.emaillistverify.com`

## Authentication

### API Key

Authenticate EmailListVerify requests with an API key from the EmailListVerify API section.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://api.emaillistverify.com/api-doc)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Blacklists](actions/check-blacklists.md) | `POST /api/checkBlacklists` | [docs](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/checkBlacklists) |
| [Check Disposable Domain](actions/check-disposable-domain.md) | `POST /api/checkDisposable` | [docs](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/checkDisposable) |
| [Create Email Verification Job](actions/create-email-verification-job.md) | `POST /api/emailJobs` | [docs](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/createEmailJob) |
| [Create Inbox Placement Test](actions/create-inbox-placement-test.md) | `POST /api/inboxPlacementTests` | [docs](https://api.emaillistverify.com/api-doc#/Inbox%20Placement%20Test%20Endpoints/createPlacementTest) |
| [Delete Email List](actions/delete-email-list.md) | `DELETE /api/maillists/:id` | [docs](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/deleteMaillist) |
| [Download Email List](actions/download-email-list.md) | `GET /api/maillists/:id` | [docs](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/downloadMaillist) |
| [Find Contact Email](actions/find-contact-email.md) | `POST /api/findContact` | [docs](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/findContact) |
| [Get Credits](actions/get-credits.md) | `GET /api/credits` | [docs](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/credits) |
| [Get Email List Progress](actions/get-email-list-progress.md) | `GET /api/maillists/:id/progress` | [docs](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/maillistProgress) |
| [Get Email Verification Job](actions/get-email-verification-job.md) | `GET /api/emailJobs/:id` | [docs](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/getEmailJob) |
| [Get Inbox Placement Test](actions/get-inbox-placement-test.md) | `GET /api/inboxPlacementTests/:code` | [docs](https://api.emaillistverify.com/api-doc#/Inbox%20Placement%20Test%20Endpoints/getPlacementTest) |
| [Upload Email List](actions/upload-email-list.md) | `POST /api/verifyApiFile` | [docs](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/verifyApiFile) |
| [Verify Email](actions/verify-email.md) | `GET /api/verifyEmail` | [docs](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/verifySingleEmail) |
| [Verify Email Detailed](actions/verify-email-detailed.md) | `GET /api/verifyEmailDetailed` | [docs](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/verifySingleEmailDetailed) |
