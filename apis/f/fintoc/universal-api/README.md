# <img src="https://images.mindcloud.co/apps/icons/idd-hq2to-o8-logos_1775148170272.jpeg" alt="Fintoc logo" width="28" height="28"> Fintoc: Universal API

Fintoc API integration for payments, transfers, direct debit, and bank movement data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fintoc/latest
- **Category:** Commerce / Accounting
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fintoc.com
- **Vendor API docs:** https://docs.fintoc.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Fintoc. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Fintoc. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Link Intent](actions/create-link-intent.md) | POST | Creates a link intent in Fintoc. |
| [Create Payment Link](actions/create-payment-link.md) | POST | Creates a payment link in Fintoc. |
| [Create Transfer](actions/create-transfer.md) | POST | Creates a transfer in Fintoc. |
| [Get Link](actions/get-link.md) | GET | Retrieves a link from Fintoc. |
| [Get Payment Intent](actions/get-payment-intent.md) | GET | Retrieves a payment intent from Fintoc. |
| [Get Transfer](actions/get-transfer.md) | GET | Retrieves a transfer from Fintoc. |
| [List Institutions](actions/list-institutions.md) | GET | Retrieves institutions from Fintoc. |
| [List Links](actions/list-links.md) | GET | Retrieves links from Fintoc. |
| [List Payment Intents](actions/list-payment-intents.md) | GET | Retrieves payment intents from Fintoc. |
| [List Payment Links](actions/list-payment-links.md) | GET | Retrieves payment links from Fintoc. |
| [List Transfers](actions/list-transfers.md) | GET | Retrieves transfers from Fintoc. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | POST | Creates a webhook endpoint in Fintoc. |
| [Get Webhook Endpoint](actions/get-webhook-endpoint.md) | GET | Retrieves a webhook endpoint from Fintoc. |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET | Retrieves webhook endpoints from Fintoc. |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | PUT | Updates a webhook endpoint in Fintoc. |

