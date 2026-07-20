# Easy Email Verification: Native API Reference

A consolidated summary of Easy Email Verification's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://eev.stoplight.io/docs/eev/902yv4tm9bfd9-easy-email-verification-api
- **OpenAPI specification:** https://stoplight.io/api/v1/projects/eev/eev/nodes/easyemail-easy-email-verification-api-v1.0.1-resolved.yaml?fromExportButton=true&snapshotType=http_service&deref=optimizedBundle
- **API base URL:** `https://api.easyemailverification.com/v1`

## Authentication

### API Key

Use your Easy Email Verification API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://eev.stoplight.io/docs/eev/d5e2c7edf080f-authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Bulk Verification Job](actions/delete-bulk-verification-job.md) | `DELETE /bulk/:id` | [docs](https://eev.stoplight.io/docs/eev/c463fbf875570-delete-a-bulk-verification-job) |
| [Download Processed Results File](actions/download-processed-results-file.md) | `GET /bulk/download/:id` | [docs](https://eev.stoplight.io/docs/eev/823978d9ab42a-download-the-processed-results-file) |
| [Get Bulk Job Status](actions/get-bulk-job-status.md) | `GET /bulk/status/:id` | [docs](https://eev.stoplight.io/docs/eev/42dd46bb7b21a-get-the-status-of-a-specific-bulk-job) |
| [List Bulk Jobs](actions/list-bulk-jobs.md) | `GET /bulk/status` | [docs](https://eev.stoplight.io/docs/eev/bb53ca38a5019-get-the-status-of-all-bulk-jobs) |
| [Upload Bulk Email File](actions/upload-bulk-email-file.md) | `POST /bulk/upload` | [docs](https://eev.stoplight.io/docs/eev/e29cb418841bc-upload-a-bulk-email-file-for-processing) |
| [Verify Email](actions/verify-email.md) | `GET /verify` | [docs](https://eev.stoplight.io/docs/eev/dfdcc20c7d4e9-lookup-a-single-email-you-can-verify-an-email-to-check-its-validity) |
| [Verify Email List](actions/verify-email-list.md) | `POST /verify` | [docs](https://eev.stoplight.io/docs/eev/ed1e2a4c4e6a1-when-you-have-list-of-emails-to-be-verified) |
