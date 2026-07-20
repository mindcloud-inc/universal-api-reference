# <img src="https://images.mindcloud.co/apps/icons/kiwify-logo-png-seeklogo-537186_1773765547319.png" alt="Kiwify logo" width="28" height="28"> Kiwify: Universal API

Kiwify lets creators sell digital products, manage affiliates, monitor sales, payouts, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kiwify/latest
- **Category:** Commerce
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kiwify.com.br
- **Vendor API docs:** https://docs.kiwify.com.br/api-reference/general

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Payouts](actions/list-payouts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/list-payouts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account details from Kiwify. |

### Affiliate

| Action | Method | Description |
| --- | --- | --- |
| [Get Affiliate](actions/get-affiliate.md) | GET | Retrieves an affiliate from Kiwify. |
| [List Affiliates](actions/list-affiliates.md) | GET | Retrieves affiliates from Kiwify. |
| [Update Affiliate](actions/update-affiliate.md) | PUT | Updates an existing affiliate in Kiwify. |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves a balance from Kiwify. |
| [List Balances](actions/list-balances.md) | GET | Retrieves balances from Kiwify. |

### Event Participant

| Action | Method | Description |
| --- | --- | --- |
| [List Event Participants](actions/list-event-participants.md) | GET | Retrieves event participants from Kiwify. |

### Payout

| Action | Method | Description |
| --- | --- | --- |
| [Create Payout](actions/create-payout.md) | POST | Creates a payout in Kiwify. |
| [Get Payout](actions/get-payout.md) | GET | Retrieves a payout from Kiwify. |
| [List Payouts](actions/list-payouts.md) | GET | Retrieves payouts from Kiwify. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Kiwify. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Kiwify. |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [Get Sale](actions/get-sale.md) | GET | Retrieves a sale from Kiwify. |
| [List Sales](actions/list-sales.md) | GET | Retrieves sales from Kiwify. |

### Sale Refund

| Action | Method | Description |
| --- | --- | --- |
| [Create Sale Refund](actions/create-sale-refund.md) | POST | Creates a sale refund in Kiwify. |

### Sale Statistic

| Action | Method | Description |
| --- | --- | --- |
| [Get Sales Stats](actions/get-sales-stats.md) | GET | Retrieves sales statistics from Kiwify. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Kiwify. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Kiwify. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Kiwify. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Kiwify. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Kiwify. |

