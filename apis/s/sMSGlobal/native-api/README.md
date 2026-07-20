# SMSGlobal: Native API Reference

A consolidated summary of SMSGlobal's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://www.smsglobal.com/rest-api/
- **API base URL:** `https://api.smsglobal.com`

## Authentication

### REST API Key + Secret

Authenticate SMSGlobal REST requests with a REST API key and REST API secret.

### Credentials

- **REST API key:** `apiKey` · required · REST API key generated from the SMSGlobal MXT API Keys page.
- **REST API secret:** `apiSecret` · required · REST API secret paired with the REST API key from the SMSGlobal MXT API Keys page.

[Official authentication documentation](https://knowledgebase.smsglobal.com/en/articles/5181990-rest-api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Auto Top-up](actions/get-auto-top-up.md) | `GET /v2/auto-topup` | [docs](https://www.smsglobal.com/rest-api/) |
| [Get Contact](actions/get-contact.md) | `GET /v2/contact/:id` | [docs](https://www.smsglobal.com/rest-api/) |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /v2/user/credit-balance` | [docs](https://www.smsglobal.com/rest-api/) |
| [Get Group](actions/get-group.md) | `GET /v2/group/:id` | [docs](https://www.smsglobal.com/rest-api/) |
| [Get Low Balance Alerts](actions/get-low-balance-alerts.md) | `GET /v2/user/low-balance-alerts` | [docs](https://www.smsglobal.com/rest-api/) |
| [Get User Billing Details](actions/get-user-billing-details.md) | `GET /v2/user/billing-details` | [docs](https://www.smsglobal.com/rest-api/) |
| [Get User Contact Details](actions/get-user-contact-details.md) | `GET /v2/user/contact-details` | [docs](https://www.smsglobal.com/rest-api/) |
| [List Dedicated Numbers](actions/list-dedicated-numbers.md) | `GET /v2/dedicated-number` | [docs](https://www.smsglobal.com/rest-api/) |
| [List Group Contacts](actions/list-group-contacts.md) | `GET /v2/group/:groupId/contacts` | [docs](https://www.smsglobal.com/rest-api/) |
| [List Groups](actions/list-groups.md) | `GET /v2/group` | [docs](https://www.smsglobal.com/rest-api/) |
| [List Incoming Messages](actions/list-incoming-messages.md) | `GET /v2/sms-incoming` | [docs](https://www.smsglobal.com/rest-api/) |
| [List Opt-Outs](actions/list-opt-outs.md) | `GET /v2/opt-outs` | [docs](https://www.smsglobal.com/rest-api/) |
| [List Outgoing Messages](actions/list-outgoing-messages.md) | `GET /v2/sms` | [docs](https://www.smsglobal.com/rest-api/) |
| [List Pending Verified Numbers](actions/list-pending-verified-numbers.md) | `GET /v2/user/verified-numbers/pending` | [docs](https://www.smsglobal.com/rest-api/) |
| [List Sender IDs](actions/list-sender-ids.md) | `GET /v2/sender-id` | [docs](https://www.smsglobal.com/rest-api/) |
| [List Shared Pools](actions/list-shared-pools.md) | `GET /v2/sharedpool` | [docs](https://www.smsglobal.com/rest-api/) |
| [List Verified Numbers](actions/list-verified-numbers.md) | `GET /v2/user/verified-numbers` | [docs](https://www.smsglobal.com/rest-api/) |
