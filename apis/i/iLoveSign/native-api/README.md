# iLoveSign: Native API Reference

A consolidated summary of iLoveSign's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://www.iloveapi.com/docs/signature-guides
- **API base URL:** `https://api.ilovepdf.com/v1`

## Authentication

### Project Token

Use an iLoveAPI project public key to obtain a short-lived bearer token for signature and task endpoints.

### Credentials

- **Public Key:** `publicKey` · required · iLoveAPI project public key used to request a bearer token.
- **Secret Key:** `secretKey` · required · iLoveAPI project secret key used for server-side task access and local JWT signing flows.
- **Project ID:** `projectId` · optional · Developer console project ID for operator reference.

Send these headers with each API request:

```http
Authorization: Bearer <custom.token>
```

[Official authentication documentation](https://www.iloveapi.com/docs/signature-guides/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate Project](actions/authenticate-project.md) | `POST /auth` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Connect Task](actions/connect-task.md) | `POST https://:server/v1/task/next` | [docs](https://www.iloveapi.com/docs/api-reference#task) |
| [Delete Task](actions/delete-task.md) | `DELETE https://:server/v1/task/:task` | [docs](https://www.iloveapi.com/docs/api-reference#task) |
| [Download Audit](actions/download-audit.md) | `GET https://:server/v1/signature/:token_requester/download-audit` | [docs](https://www.iloveapi.com/docs/api-reference#download-audit) |
| [Download Original Files](actions/download-original-files.md) | `GET https://:server/v1/signature/:token_requester/download-original` | [docs](https://www.iloveapi.com/docs/api-reference#download-original) |
| [Download Signed Files](actions/download-signed-files.md) | `GET https://:server/v1/signature/:token_requester/download-signed` | [docs](https://www.iloveapi.com/docs/api-reference#download-signed) |
| [Fix Receiver Email](actions/fix-receiver-email.md) | `PUT /signature/receiver/fix-email/:receiver_token_requester` | [docs](https://www.iloveapi.com/docs/api-reference#fix-signer-email) |
| [Fix Signer Phone](actions/fix-signer-phone.md) | `PUT /signature/signer/fix-phone/:signer_token_requester` | [docs](https://www.iloveapi.com/docs/api-reference#fix-signer-phone) |
| [Get Receiver Info](actions/get-receiver-info.md) | `GET /signature/receiver/info/:receiver_token_requester` | [docs](https://www.iloveapi.com/docs/api-reference#get-signer) |
| [Get Signature Status](actions/get-signature-status.md) | `GET /signature/requesterview/:token_requester` | [docs](https://www.iloveapi.com/docs/api-reference#get-signature) |
| [Increase Expiration Days](actions/increase-expiration-days.md) | `PUT /signature/increase-expiration-days/:token_requester` | [docs](https://www.iloveapi.com/docs/api-reference#signature-increase-expiration-days) |
| [List Signatures](actions/list-signatures.md) | `GET /signature/list` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [List Tasks](actions/list-tasks.md) | `POST /task` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Remove Uploaded File](actions/remove-uploaded-file.md) | `DELETE https://:server/v1/upload/:task/:server_filename` | [docs](https://www.iloveapi.com/docs/api-reference#upload) |
| [Send Reminder](actions/send-reminder.md) | `POST /signature/sendReminder/:token_requester` | [docs](https://www.iloveapi.com/docs/api-reference#send-reminders) |
| [Start Sign Task](actions/start-sign-task.md) | `GET /start/sign` | [docs](https://www.iloveapi.com/docs/api-reference#create-signature) |
| [Upload File From URL](actions/upload-file-from-url.md) | `POST https://:server/v1/upload` | [docs](https://www.iloveapi.com/docs/api-reference#upload) |
| [Void Signature](actions/void-signature.md) | `PUT /signature/void/:token_requester` | [docs](https://www.iloveapi.com/docs/api-reference#signature-void) |
