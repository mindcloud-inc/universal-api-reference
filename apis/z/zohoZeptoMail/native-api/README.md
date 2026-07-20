# Zoho ZeptoMail: Native API Reference

A consolidated summary of Zoho ZeptoMail's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/zeptomail/help/api-index.html
- **API base URL:** `https://api.zeptomail.com/v1.1`

## Authentication

### OAuth2

Use Zoho OAuth 2.0 for ZeptoMail management APIs such as domains, templates, suppressions, exports, and email logs.

### Credentials

- **Agent Alias:** `agentAlias` · required · Mail Agent alias used by ZeptoMail template APIs and agent-scoped operations.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `Zeptomail.Suppressions.All`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/accounts/protocol/oauth/web-server-applications.html)

### Send Mail Token

Use a ZeptoMail Mail Agent send mail token for email-sending and file-cache APIs.

### Credentials

- **API Key:** `apiKey` · required
- **Agent Alias:** `agentAlias` · required · Mail Agent alias used by ZeptoMail template APIs and agent-scoped operations.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.zoho.com/zeptomail/help/API-home.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Domain](actions/add-domain.md) | `POST domains` | [docs](https://www.zoho.com/zeptomail/help/api/add-domain.html) |
| [Add Suppression](actions/add-suppression.md) | `POST suppressions/:type` | [docs](https://www.zoho.com/zeptomail/help/api/add-suppression-list.html) |
| [Add Template](actions/add-template.md) | `POST agents/:agentAlias/templates` | [docs](https://www.zoho.com/zeptomail/help/api/add-template.html) |
| [Create Export](actions/create-export.md) | `POST :exportType/exports` | [docs](https://www.zoho.com/zeptomail/help/api/export-logs.html) |
| [Delete Suppression](actions/delete-suppression.md) | `DELETE suppressions/:type` | [docs](https://www.zoho.com/zeptomail/help/api/delete-suppression-list.html) |
| [Delete Template](actions/delete-template.md) | `DELETE agents/:agentAlias/templates/:templateKey` | [docs](https://www.zoho.com/zeptomail/help/api/delete-template.html) |
| [Download Export](actions/download-export.md) | `GET :exportType/exports/:exportId/download` | [docs](https://www.zoho.com/zeptomail/help/api/download-exports.html) |
| [Edit Suppression](actions/edit-suppression.md) | `PUT suppressions/:type` | [docs](https://www.zoho.com/zeptomail/help/api/edit-suppression-list.html) |
| [Get Domain](actions/get-domain.md) | `GET domains/:domainKey` | [docs](https://www.zoho.com/zeptomail/help/api/get-specific-domain.html) |
| [Get Email Log](actions/get-email-log.md) | `GET email/email-reference/:emailReference` | [docs](https://www.zoho.com/zeptomail/help/api/get-specific-email-log.html) |
| [Get Template](actions/get-template.md) | `GET agents/:agentAlias/templates/:templateKey` | [docs](https://www.zoho.com/zeptomail/help/api/get-template.html) |
| [List Domains](actions/list-domains.md) | `GET domains` | [docs](https://www.zoho.com/zeptomail/help/api/list-all-domains.html) |
| [List Email Logs](actions/list-email-logs.md) | `GET email` | [docs](https://www.zoho.com/zeptomail/help/api/get-email-logs.html) |
| [List Exports](actions/list-exports.md) | `GET :exportType/exports` | [docs](https://www.zoho.com/zeptomail/help/api/fetch-exports.html) |
| [List Suppressions](actions/list-suppressions.md) | `GET suppressions/:type` | [docs](https://www.zoho.com/zeptomail/help/api/get-suppression-list.html) |
| [List Templates](actions/list-templates.md) | `GET agents/:agentAlias/templates` | [docs](https://www.zoho.com/zeptomail/help/api/list-template.html) |
| [Send Batch Email](actions/send-batch-email.md) | `POST email/batch` | [docs](https://www.zoho.com/zeptomail/help/api/batch-email-sending.html) |
| [Send Batch Email with Template](actions/send-batch-email-with-template.md) | `POST email/template/batch` | [docs](https://www.zoho.com/zeptomail/help/api/batch-email-templates.html) |
| [Send Email](actions/send-email.md) | `POST email` | [docs](https://www.zoho.com/zeptomail/help/api/email-sending.html) |
| [Send Email with Template](actions/send-email-with-template.md) | `POST email/template` | [docs](https://www.zoho.com/zeptomail/help/api/email-templates.html) |
| [Update Domain](actions/update-domain.md) | `PUT domains/:domainKey` | [docs](https://www.zoho.com/zeptomail/help/api/edit-domain.html) |
| [Update Template](actions/update-template.md) | `PUT agents/:agentAlias/templates/:templateKey` | [docs](https://www.zoho.com/zeptomail/help/api/update-template.html) |
| [Upload File to Cache](actions/upload-file-to-cache.md) | `POST files` | [docs](https://www.zoho.com/zeptomail/help/api/file-upload.html) |
| [Verify Domain](actions/verify-domain.md) | `PUT domains/:domainKey/verify` | [docs](https://www.zoho.com/zeptomail/help/api/verify-domain.html) |
