# Evervault: Native API Reference

A consolidated summary of Evervault's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.evervault.com/api
- **OpenAPI specification:** https://docs.evervault.com/api-spec.json
- **API base URL:** `https://api.evervault.com`

## Authentication

### Basic Auth

Use Evervault app_id as username and api_key as password (HTTP Basic Auth).

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.evervault.com/api#authentication)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [BIN Lookup](actions/bin-lookup.md) | `POST /payments/bin-lookups` | [docs](https://docs.evervault.com/api#createBinLookup) |
| [Card Insights](actions/card-insights.md) | `POST /insights/cards` | [docs](https://docs.evervault.com/api#createCardInsight) |
| [Create Client Token](actions/create-client-token.md) | `POST /client-side-tokens` | [docs](https://docs.evervault.com/api#create-client-side-token) |
| [Create Merchant](actions/create-merchant.md) | `POST /payments/merchants` | [docs](https://docs.evervault.com/api#createMerchant) |
| [Create Relay](actions/create-relay.md) | `POST /relays` | [docs](https://docs.evervault.com/api#createRelay) |
| [Create Relay Custom Domain](actions/create-relay-custom-domain.md) | `POST /relays/{relay_id}/custom-domains` | [docs](https://docs.evervault.com/api#createCustomDomain) |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | `POST /webhook-endpoints` | [docs](https://docs.evervault.com/api#createWebhookEndpoint) |
| [Decrypt Data](actions/decrypt-data.md) | `POST /decrypt` | [docs](https://docs.evervault.com/api#decrypt) |
| [Delete Relay](actions/delete-relay.md) | `DELETE /relays/{id}` | [docs](https://docs.evervault.com/api#deleteRelay) |
| [Delete Relay Custom Domain](actions/delete-relay-custom-domain.md) | `DELETE /relays/{relay_id}/custom-domains/{id}` | [docs](https://docs.evervault.com/api#deleteCustomDomain) |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | `DELETE /webhook-endpoints/{webhook_endpoint_id}` | [docs](https://docs.evervault.com/api#deleteWebhookEndpoint) |
| [Encrypt Data](actions/encrypt-data.md) | `POST /encrypt` | [docs](https://docs.evervault.com/api#encrypt) |
| [Inspect Token Metadata](actions/inspect-token-metadata.md) | `POST /inspect` | [docs](https://docs.evervault.com/api#inspect) |
| [List Merchants](actions/list-merchants.md) | `GET /payments/merchants` | [docs](https://docs.evervault.com/api#listMerchants) |
| [List Relay Custom Domains](actions/list-relay-custom-domains.md) | `GET /relays/{relay_id}/custom-domains` | [docs](https://docs.evervault.com/api#fetchCustomDomainsForRelay) |
| [List Relays](actions/list-relays.md) | `GET /relays` | [docs](https://docs.evervault.com/api#listRelays) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET /webhook-endpoints` | [docs](https://docs.evervault.com/api#listWebhookEndpoints) |
| [Retrieve Merchant](actions/retrieve-merchant.md) | `GET /payments/merchants/{merchant_id}` | [docs](https://docs.evervault.com/api#getMerchant) |
| [Retrieve Relay](actions/retrieve-relay.md) | `GET /relays/{id}` | [docs](https://docs.evervault.com/api#fetchRelay) |
| [Retrieve Relay Custom Domain](actions/retrieve-relay-custom-domain.md) | `GET /relays/{relay_id}/custom-domains/{id}` | [docs](https://docs.evervault.com/api#retrieveCustomDomain) |
| [Retrieve Webhook Endpoint](actions/retrieve-webhook-endpoint.md) | `GET /webhook-endpoints/{webhook_endpoint_id}` | [docs](https://docs.evervault.com/api#getWebhookEndpoint) |
| [Run Function](actions/run-function.md) | `POST /functions/{function_name}/runs` | [docs](https://docs.evervault.com/api#createFunctionRun) |
| [Update Relay](actions/update-relay.md) | `PATCH /relays/{id}` | [docs](https://docs.evervault.com/api#updateRelay) |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | `PATCH /webhook-endpoints/{webhook_endpoint_id}` | [docs](https://docs.evervault.com/api#updateWebhookEndpoint) |
