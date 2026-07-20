# Listclean: Native API Reference

A consolidated summary of Listclean's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://api.listclean.xyz/
- **OpenAPI specification:** https://api.listclean.xyz/v1/spec.json
- **API base URL:** `https://api.listclean.xyz/v1`

## Authentication

### Listclean API Token

Authenticate Listclean API requests with the API token sent in the X-Auth-Token request header.

### Credentials

- **API Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.listclean.xyz/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete List](actions/delete-list.md) | `DELETE /lists/:list_id` | [docs](https://api.listclean.xyz/) |
| [Download List Results As CSV](actions/download-list-results-as-csv.md) | `GET /downloads/:list_id/:type` | [docs](https://api.listclean.xyz/) |
| [Download List Results As JSON](actions/download-list-results-as-json.md) | `GET /downloads/json/:list_id/:type` | [docs](https://api.listclean.xyz/) |
| [Get Account Profile](actions/get-account-profile.md) | `GET /account/profile/` | [docs](https://api.listclean.xyz/) |
| [Get List Information](actions/get-list-information.md) | `GET /lists/:list_id` | [docs](https://api.listclean.xyz/) |
| [Get Remaining Credits](actions/get-remaining-credits.md) | `GET /credits` | [docs](https://api.listclean.xyz/) |
| [Get Upload Status](actions/get-upload-status.md) | `GET /uploads/:upload_id` | [docs](https://api.listclean.xyz/) |
| [Get Verification Logs](actions/get-verification-logs.md) | `GET /verify/email/logs` | [docs](https://api.listclean.xyz/) |
| [List All Verification Lists](actions/list-all-verification-lists.md) | `GET /lists/` | [docs](https://api.listclean.xyz/) |
| [List CSV Uploads](actions/list-csv-uploads.md) | `GET /uploads/` | [docs](https://api.listclean.xyz/) |
| [Start Upload](actions/start-upload.md) | `POST /uploads/` | [docs](https://api.listclean.xyz/) |
| [Update Account Profile](actions/update-account-profile.md) | `POST /account/profile/` | [docs](https://api.listclean.xyz/) |
| [Upload Chunk](actions/upload-chunk.md) | `POST /uploads/:upload_id` | [docs](https://api.listclean.xyz/) |
| [Verify Batch Of Emails](actions/verify-batch-of-emails.md) | `POST /verify/email/batch` | [docs](https://api.listclean.xyz/) |
| [Verify Email Address](actions/verify-email-address.md) | `GET /verify/email/:email` | [docs](https://api.listclean.xyz/) |
