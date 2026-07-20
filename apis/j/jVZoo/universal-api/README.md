# <img src="https://images.mindcloud.co/apps/icons/j-vzoo_1773868727536.png" alt="JVZoo logo" width="28" height="28"> JVZoo: Universal API

Manage JVZoo transactions, affiliates, and recurring payments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jVZoo/latest
- **Category:** Commerce
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.jvzoo.com
- **Vendor API docs:** https://api.jvzoo.com/docs/versions/v2.0.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Latest Transactions](actions/get-latest-transactions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/get-latest-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Affiliate

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Affiliate Status](actions/retrieve-affiliate-status.md) | GET | Retrieves affiliate status for a JVZoo product. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Recurring Payment](actions/cancel-recurring-payment.md) | PUT | Cancels a recurring payment in JVZoo. |
| [Get Recurring Payment Status](actions/get-recurring-payment-status.md) | GET | Retrieves recurring payment status from JVZoo. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Affiliate Transactions](actions/get-affiliate-transactions.md) | GET | Retrieves your latest affiliate transactions from JVZoo. |
| [Get Latest Transactions](actions/get-latest-transactions.md) | GET | Retrieves latest transactions across your JVZoo products. |
| [Get Transaction Summary](actions/get-transaction-summary.md) | GET | Retrieves a transaction summary from JVZoo. |

