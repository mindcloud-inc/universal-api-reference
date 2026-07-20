# Postmark: Native API Reference

A consolidated summary of Postmark's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://postmarkapp.com/developer/api/overview
- **API base URL:** `https://api.postmarkapp.com`

## Authentication

### Postmark API Tokens

Use your Postmark server token for server-scoped endpoints and your account token for account-scoped endpoints.

### Credentials

- **API Key:** `apiKey` · required
- **Account Token:** `accountToken` · required · Required for Postmark account-scoped endpoints such as servers, domains, and sender signatures.

Send these headers with each API request:

```http
X-Postmark-Account-Token: <accountToken>
```

[Official authentication documentation](https://postmarkapp.com/developer/api/overview)

### Postmark Dual Tokens

Use a Postmark server token for server-scoped endpoints and an account token for account-scoped endpoints.

### Credentials

- **Server Token:** `serverToken` · required · Required for server-scoped endpoints such as templates, messages, bounces, stats, and email sends.
- **Account Token:** `accountToken` · required · Required for account-scoped endpoints such as servers, sender signatures, and domains.

Send these headers with each API request:

```http
X-Postmark-Server-Token: <serverToken>
X-Postmark-Account-Token: <accountToken>
```

[Official authentication documentation](https://postmarkapp.com/developer/api/overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `count` in the query string to set the page size (default 100; accepted range 1–500). Use `offset` in the query string as the record offset.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | `POST /domains` | [docs](https://postmarkapp.com/developer/api/domains-api#create-domain) |
| [Create Sender Signature](actions/create-sender-signature.md) | `POST /senders` | [docs](https://postmarkapp.com/developer/api/signatures-api#create-signature) |
| [Create Server](actions/create-server.md) | `POST /servers` | [docs](https://postmarkapp.com/developer/api/servers-api#create-server) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://postmarkapp.com/developer/api/templates-api#create-template) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/:templateIdOrAlias` | [docs](https://postmarkapp.com/developer/api/templates-api#delete-template) |
| [Get Bounce](actions/get-bounce.md) | `GET /bounces/:bounceId` | [docs](https://postmarkapp.com/developer/api/bounce-api#single-bounce) |
| [Get Delivery Stats](actions/get-delivery-stats.md) | `GET /deliverystats` | [docs](https://postmarkapp.com/developer/api/bounce-api#delivery-stats) |
| [Get Domain](actions/get-domain.md) | `GET /domains/:domainId` | [docs](https://postmarkapp.com/developer/api/domains-api#domain) |
| [Get Outbound Message Details](actions/get-outbound-message-details.md) | `GET /messages/outbound/:messageId/details` | [docs](https://postmarkapp.com/developer/api/messages-api#outbound-message-details) |
| [Get Outbound Stats Overview](actions/get-outbound-stats-overview.md) | `GET /stats/outbound` | [docs](https://postmarkapp.com/developer/api/stats-api#overview) |
| [Get Sender Signature](actions/get-sender-signature.md) | `GET /senders/:signatureId` | [docs](https://postmarkapp.com/developer/api/signatures-api#sender-signature) |
| [Get Server](actions/get-server.md) | `GET /servers/:serverId` | [docs](https://postmarkapp.com/developer/api/servers-api#get-server) |
| [Get Server Configuration](actions/get-server-configuration.md) | `GET /server` | [docs](https://postmarkapp.com/developer/api/server-api#get-server) |
| [Get Template](actions/get-template.md) | `GET /templates/:templateIdOrAlias` | [docs](https://postmarkapp.com/developer/api/templates-api#get-template) |
| [List Bounces](actions/list-bounces.md) | `GET /bounces` | [docs](https://postmarkapp.com/developer/api/bounce-api#bounces) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://postmarkapp.com/developer/api/domains-api#list-domains) |
| [List Sender Signatures](actions/list-sender-signatures.md) | `GET /senders` | [docs](https://postmarkapp.com/developer/api/signatures-api#list-sender-signatures) |
| [List Servers](actions/list-servers.md) | `GET /servers` | [docs](https://postmarkapp.com/developer/api/servers-api#list-servers) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://postmarkapp.com/developer/api/templates-api#list-templates) |
| [Reactivate Bounce](actions/reactivate-bounce.md) | `PUT /bounces/:bounceId/activate` | [docs](https://postmarkapp.com/developer/api/bounce-api#activate-bounce) |
| [Search Outbound Messages](actions/search-outbound-messages.md) | `GET /messages/outbound` | [docs](https://postmarkapp.com/developer/api/messages-api#outbound-message-search) |
| [Send Batch Emails](actions/send-batch-emails.md) | `POST /email/batch` | [docs](https://postmarkapp.com/developer/api/email-api#send-batch-emails) |
| [Send Batch Template Emails](actions/send-batch-template-emails.md) | `POST /email/batchWithTemplates` | [docs](https://postmarkapp.com/developer/api/templates-api#send-batch-with-templates) |
| [Send Email](actions/send-email.md) | `POST /email` | [docs](https://postmarkapp.com/developer/api/email-api#send-a-single-email) |
| [Send Template Email](actions/send-template-email.md) | `POST /email/withTemplate` | [docs](https://postmarkapp.com/developer/api/templates-api#email-with-template) |
| [Update Sender Signature](actions/update-sender-signature.md) | `PUT /senders/:signatureId` | [docs](https://postmarkapp.com/developer/api/signatures-api#edit-signature) |
| [Update Server](actions/update-server.md) | `PUT /servers/:serverId` | [docs](https://postmarkapp.com/developer/api/servers-api#edit-server) |
| [Update Server Configuration](actions/update-server-configuration.md) | `PUT /server` | [docs](https://postmarkapp.com/developer/api/server-api#edit-server) |
| [Update Template](actions/update-template.md) | `PUT /templates/:templateIdOrAlias` | [docs](https://postmarkapp.com/developer/api/templates-api#edit-template) |
| [Validate Template](actions/validate-template.md) | `POST /templates/validate` | [docs](https://postmarkapp.com/developer/api/templates-api#validate-template) |
