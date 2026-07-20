# CINCEL: Native API Reference

A consolidated summary of CINCEL's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://docs.cincel.digital/v3/digital-signature
- **OpenAPI specification:** https://api.cincel.digital/v3/oas.yaml?tags=digital-signature,auth,tokens
- **API base URL:** `https://api.cincel.digital/v3`

## Authentication

### Bearer JWT

Use a current CINCEL JWT generated from the OTP exchange.

### Credentials

- **JWT:** `jwt` · required · Paste the current CINCEL JWT returned by GET /tokens/jwt.
- **Email:** `email` · required · CINCEL account email used for the OTP and JWT token endpoints.
- **OTP:** `otp` · optional · Current one-time password from the CINCEL email, used only for GET /tokens/jwt.
- **Request OTP Basic Auth:** `requestOtpBasicAuth` · optional · Base64-encoded email: value used by GET /tokens/otp when the runner cannot inline-encode Basic auth.
- **Exchange JWT Basic Auth:** `exchangeJwtBasicAuth` · optional · Base64-encoded email:otp value used by GET /tokens/jwt when the runner cannot inline-encode Basic auth.

Send these headers with each API request:

```http
Authorization: Bearer <jwt>
```

[Official authentication documentation](https://api.cincel.digital/v3/oas.yaml?tags=digital-signature,auth,tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 1001; accepted range 1–1000000). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /teams/:team/contacts` | [docs](https://docs.cincel.digital/v3/digital-signature#post-/teams/-team-/contacts) |
| [Create Document Invite](actions/create-document-invite.md) | `POST /teams/:team/folders/:folder/documents/:document/invites` | [docs](https://docs.cincel.digital/v3/digital-signature#post-/teams/-team-/folders/-folder-/documents/-document-/invites) |
| [Create Folder](actions/create-folder.md) | `POST /teams/:team/folders` | [docs](https://docs.cincel.digital/v3/digital-signature#post-/teams/-team-/folders) |
| [Delete Document Invite](actions/delete-document-invite.md) | `DELETE /teams/:team/folders/:folder/documents/:document/invites/:invite` | [docs](https://docs.cincel.digital/v3/digital-signature#delete-/teams/-team-/folders/-folder-/documents/-document-/invites/-invite-) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /teams/:team/folders/:folder` | [docs](https://docs.cincel.digital/v3/digital-signature#delete-/teams/-team-/folders/-folder-) |
| [Download Audit Trail PDF](actions/download-audit-trail-pdf.md) | `GET /teams/:team/folders/:folder/documents/:document/audit-trail.pdf` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders/-folder-/documents/-document-/audit-trail.pdf) |
| [Download Document Evidence ZIP](actions/download-document-evidence-zip.md) | `GET /documents/:document.zip` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/documents/-document-.zip) |
| [Download Original Document PDF](actions/download-original-document-pdf.md) | `GET /teams/:team/folders/:folder/documents/:document.pdf` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders/-folder-/documents/-document-.pdf) |
| [Download Signed Document PDF](actions/download-signed-document-pdf.md) | `GET /documents/:document/signed-document.pdf` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/documents/-document-/signed-document.pdf) |
| [Download Team Signed Documents ZIP](actions/download-team-signed-documents-zip.md) | `GET /teams/:team/:takeout.zip` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/-takeout-.zip) |
| [Exchange OTP For JWT](actions/exchange-otp-for-jwt.md) | `GET /tokens/jwt` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/tokens/jwt) |
| [Get Document Invite](actions/get-document-invite.md) | `GET /teams/:team/folders/:folder/documents/:document/invites/:invite` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders/-folder-/documents/-document-/invites/-invite-) |
| [Get Folder](actions/get-folder.md) | `GET /teams/:team/folders/:folder` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders/-folder-) |
| [Get Invite Signing Token](actions/get-invite-signing-token.md) | `GET /teams/:team/folders/:folder/documents/:document/invites/:invite/token` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders/-folder-/documents/-document-/invites/-invite-/token) |
| [Get Team](actions/get-team.md) | `GET /teams/:uuid` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/teams/-uuid-) |
| [Get Team Credits](actions/get-team-credits.md) | `GET /teams/:team/credits` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/credits) |
| [Get Timestamp Or Certificate Artifact](actions/get-timestamp-or-certificate-artifact.md) | `GET /teams/:team/folders/:folder/documents/:document/:timestamp` | [docs](https://docs.cincel.digital/v3/digital-signature) |
| [List Document Invites](actions/list-document-invites.md) | `GET /teams/:team/folders/:folder/documents/:document/invites` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders/-folder-/documents/-document-/invites) |
| [List Folders](actions/list-folders.md) | `GET /teams/:team/folders` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders) |
| [List Team Users](actions/list-team-users.md) | `GET /teams/:team/users` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/users) |
| [List User Documents](actions/list-user-documents.md) | `GET /users/:user/documents` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/users/-user-/documents) |
| [List User Teams](actions/list-user-teams.md) | `GET /users/:user/teams` | [docs](https://api.cincel.digital/v3/oas.yaml?tags=digital-signature,auth,tokens) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/users) |
| [Request OTP](actions/request-otp.md) | `GET /tokens/otp` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/tokens/otp) |
| [Send Invite Reminder](actions/send-invite-reminder.md) | `GET /teams/:team/folders/:folder/documents/:document/invites/:invite/notification` | [docs](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders/-folder-/documents/-document-/invites/-invite-/notification) |
| [Update Document Invite](actions/update-document-invite.md) | `PATCH /teams/:team/folders/:folder/documents/:document/invites/:invite` | [docs](https://docs.cincel.digital/v3/digital-signature#patch-/teams/-team-/folders/-folder-/documents/-document-/invites/-invite-) |
| [Update Folder](actions/update-folder.md) | `PATCH /teams/:team/folders/:folder` | [docs](https://docs.cincel.digital/v3/digital-signature#patch-/teams/-team-/folders/-folder-) |
