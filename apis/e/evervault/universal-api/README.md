# <img src="https://images.mindcloud.co/apps/icons/evervault_1775241472289.png" alt="Evervault logo" width="28" height="28"> Evervault: Universal API

Evervault API wrapper for encryption, relay management, webhook endpoints, and selected payments operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/evervault/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://evervault.com
- **Vendor API docs:** https://docs.evervault.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Relays](actions/list-relays.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/list-relays?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Binlookup

| Action | Method | Description |
| --- | --- | --- |
| [BIN Lookup](actions/bin-lookup.md) | GET | Retrieves BIN lookup details from Evervault. |

### Cardinsight

| Action | Method | Description |
| --- | --- | --- |
| [Card Insights](actions/card-insights.md) | GET | Retrieves payment card insights from Evervault. |

### Clienttoken

| Action | Method | Description |
| --- | --- | --- |
| [Create Client Token](actions/create-client-token.md) | POST | Creates a client token in Evervault. |

### Core

| Action | Method | Description |
| --- | --- | --- |
| [Decrypt Data](actions/decrypt-data.md) | GET | Decrypts previously encrypted data with Evervault. |
| [Encrypt Data](actions/encrypt-data.md) | POST | Encrypts submitted data using Evervault encryption. |

### Function

| Action | Method | Description |
| --- | --- | --- |
| [Run Function](actions/run-function.md) | POST | Creates a function run in Evervault. |

### Merchant

| Action | Method | Description |
| --- | --- | --- |
| [Create Merchant](actions/create-merchant.md) | POST | Creates a new merchant in Evervault. |
| [List Merchants](actions/list-merchants.md) | GET | Retrieves all payment merchants from Evervault. |
| [Retrieve Merchant](actions/retrieve-merchant.md) | GET | Retrieves a merchant from Evervault. |

### Relay

| Action | Method | Description |
| --- | --- | --- |
| [Create Relay](actions/create-relay.md) | POST | Creates a new relay in Evervault. |
| [Delete Relay](actions/delete-relay.md) | DELETE | Deletes an existing relay from Evervault. |
| [List Relays](actions/list-relays.md) | GET | Retrieves all configured relays from Evervault. |
| [Retrieve Relay](actions/retrieve-relay.md) | GET | Retrieves a relay from Evervault. |
| [Update Relay](actions/update-relay.md) | PUT | Updates an existing relay in Evervault. |

### Relaycustomdomain

| Action | Method | Description |
| --- | --- | --- |
| [Create Relay Custom Domain](actions/create-relay-custom-domain.md) | POST | Creates a relay custom domain in Evervault. |
| [Delete Relay Custom Domain](actions/delete-relay-custom-domain.md) | DELETE | Deletes an existing relay custom domain from Evervault. |
| [List Relay Custom Domains](actions/list-relay-custom-domains.md) | GET | Retrieves relay custom domains from Evervault. |
| [Retrieve Relay Custom Domain](actions/retrieve-relay-custom-domain.md) | GET | Retrieves a relay custom domain from Evervault. |

### Tokeninspection

| Action | Method | Description |
| --- | --- | --- |
| [Inspect Token Metadata](actions/inspect-token-metadata.md) | GET | Retrieves metadata for an encrypted token from Evervault. |

### Webhookendpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | POST | Creates a webhook endpoint in Evervault. |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | DELETE | Deletes an existing webhook endpoint from Evervault. |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET | Retrieves all webhook endpoints from Evervault. |
| [Retrieve Webhook Endpoint](actions/retrieve-webhook-endpoint.md) | GET | Retrieves a webhook endpoint from Evervault. |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | PUT | Updates an existing webhook endpoint in Evervault. |

