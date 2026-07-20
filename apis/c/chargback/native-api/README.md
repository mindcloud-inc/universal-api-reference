# Chargback: Native API Reference

A consolidated summary of Chargback's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://api.chargeback.io/api/public/docs/
- **API base URL:** `https://api.chargeback.io`

## Authentication

### API Key

Use a Chargeback public API key. Main public endpoints authenticate with X-API-KEY; JWT is only used to manage API keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://api.chargeback.io/api/public/docs/)

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Alert Status](actions/change-alert-status.md) | `PATCH /api/public/v1/alerts/:external_id/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [Create API Key](actions/create-api-key.md) | `POST /api/public/v1/api-keys/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /api/webhook/subscriptions/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [Delete API Key](actions/delete-api-key.md) | `DELETE /api/public/v1/api-keys/delete/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /api/webhook/subscriptions/:id/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [Get Alert](actions/get-alert.md) | `GET /api/public/v1/alerts/:external_id/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [Get Business Account](actions/get-business-account.md) | `GET /api/public/v1/business_accounts/:external_id/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | `GET /api/webhook/subscriptions/:id/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [List Alerts](actions/list-alerts.md) | `GET /api/public/v1/alerts/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [List API Keys](actions/list-api-keys.md) | `GET /api/public/v1/api-keys/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [List Business Accounts](actions/list-business-accounts.md) | `GET /api/public/v1/business_accounts/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [List Invoices](actions/list-invoices.md) | `GET /api/public/v1/invoices/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /api/webhook/subscriptions/` | [docs](https://api.chargeback.io/api/public/docs/) |
| [Regenerate API Key](actions/regenerate-api-key.md) | `PATCH /api/public/v1/api-keys/regenerate/` | [docs](https://api.chargeback.io/api/public/docs/) |
