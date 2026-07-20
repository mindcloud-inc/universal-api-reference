# Faraday: Native API Reference

A consolidated summary of Faraday's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://faraday.ai/docs/reference
- **API base URL:** `https://api.faraday.ai/v1`

## Authentication

### API Key

Use your Faraday API key. MindCloud sends it as Authorization: Bearer <apiKey>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://faraday.ai/docs/reference)

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Stream](actions/archive-stream.md) | `POST /streams/:stream_id_or_name/archive` | [docs](https://faraday.ai/docs/reference/archivestream) |
| [Archive Trait](actions/archive-trait.md) | `POST /traits/:trait_id/archive` | [docs](https://faraday.ai/docs/reference/archivetrait) |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://faraday.ai/docs/reference/createaccount) |
| [Create Stream](actions/create-stream.md) | `POST /streams/:stream_name` | [docs](https://faraday.ai/docs/reference/findorcreatestream) |
| [Create Trait](actions/create-trait.md) | `POST /traits` | [docs](https://faraday.ai/docs/reference/createtrait) |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | `POST /webhook_endpoints` | [docs](https://faraday.ai/docs/reference/createwebhookendpoint) |
| [Delete Account](actions/delete-account.md) | `DELETE /accounts/:account_id` | [docs](https://faraday.ai/docs/reference/deleteaccount) |
| [Delete Stream](actions/delete-stream.md) | `DELETE /streams/:stream_id_or_name` | [docs](https://faraday.ai/docs/reference/deletestream) |
| [Delete Trait](actions/delete-trait.md) | `DELETE /traits/:trait_id` | [docs](https://faraday.ai/docs/reference/deletetrait) |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | `DELETE /webhook_endpoints/:webhook_endpoint_id` | [docs](https://faraday.ai/docs/reference/deletewebhookendpoint) |
| [Force Update Stream](actions/force-update-stream.md) | `POST /streams/:stream_id_or_name/force_update` | [docs](https://faraday.ai/docs/reference/forceupdatestream) |
| [Force Update Trait](actions/force-update-trait.md) | `POST /traits/:trait_id/force_update` | [docs](https://faraday.ai/docs/reference/forceupdatetrait) |
| [Get Account Usage](actions/get-account-usage.md) | `GET /accounts/:account_id/usage` | [docs](https://faraday.ai/docs/reference/getaccountusage) |
| [Get Current Account Billing](actions/get-current-account-billing.md) | `GET /accounts/current/billing` | [docs](https://faraday.ai/docs/reference/getcurrentaccountbilling) |
| [Get Current Account Usage](actions/get-current-account-usage.md) | `GET /accounts/current/usage` | [docs](https://faraday.ai/docs/reference/getaccountcurrentusage) |
| [Get Stream](actions/get-stream.md) | `GET /streams/:stream_id_or_name` | [docs](https://faraday.ai/docs/reference/getstream) |
| [Get Stream Analysis](actions/get-stream-analysis.md) | `GET /streams/:stream_id_or_name/analysis` | [docs](https://faraday.ai/docs/reference/getstreamanalysis) |
| [Get Trait](actions/get-trait.md) | `GET /traits/:trait_id` | [docs](https://faraday.ai/docs/reference/gettrait) |
| [Get Trait Analysis Dimensions](actions/get-trait-analysis-dimensions.md) | `GET /traits/:trait_id/analysis/dimensions` | [docs](https://faraday.ai/docs/reference/gettraitanalysisdimensions) |
| [Get Usage Stats](actions/get-usage-stats.md) | `GET /usages` | [docs](https://faraday.ai/docs/reference/getusages) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://faraday.ai/docs/reference/getaccounts) |
| [List Streams](actions/list-streams.md) | `GET /streams` | [docs](https://faraday.ai/docs/reference/getstreams) |
| [List Traits](actions/list-traits.md) | `GET /traits` | [docs](https://faraday.ai/docs/reference/gettraits) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET /webhook_endpoints` | [docs](https://faraday.ai/docs/reference/getwebhookendpoints) |
| [Retrieve Account](actions/retrieve-account.md) | `GET /accounts/:account_id` | [docs](https://faraday.ai/docs/reference/getaccount) |
| [Retrieve Current Account](actions/retrieve-current-account.md) | `GET /accounts/current` | [docs](https://faraday.ai/docs/reference/getcurrentaccount) |
| [Retrieve Webhook Endpoint](actions/retrieve-webhook-endpoint.md) | `GET /webhook_endpoints/:webhook_endpoint_id` | [docs](https://faraday.ai/docs/reference/getwebhookendpoint) |
| [Unarchive Stream](actions/unarchive-stream.md) | `POST /streams/:stream_id_or_name/unarchive` | [docs](https://faraday.ai/docs/reference/unarchivestream) |
| [Unarchive Trait](actions/unarchive-trait.md) | `POST /traits/:trait_id/unarchive` | [docs](https://faraday.ai/docs/reference/unarchivetrait) |
| [Update Account](actions/update-account.md) | `PATCH /accounts/:account_id` | [docs](https://faraday.ai/docs/reference/updateaccount) |
| [Update Trait](actions/update-trait.md) | `PATCH /traits/:trait_id` | [docs](https://faraday.ai/docs/reference/updatetrait) |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | `PATCH /webhook_endpoints/:webhook_endpoint_id` | [docs](https://faraday.ai/docs/reference/updatewebhookendpoint) |
