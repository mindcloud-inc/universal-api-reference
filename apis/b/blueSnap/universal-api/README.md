# <img src="https://images.mindcloud.co/apps/icons/blue-snap_1775151005583.png" alt="BlueSnap logo" width="28" height="28"> BlueSnap: Universal API

BlueSnap is a global payment platform for processing card and alternative payments through the BlueSnap Payment API and related merchant services.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blueSnap/latest
- **Category:** Commerce
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bluesnap.com/
- **Vendor API docs:** https://developers.bluesnap.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Plans](actions/list-plans.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Card Info](actions/retrieve-card-info.md) | GET | Retrieves card information from BlueSnap. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Vaulted Shopper](actions/retrieve-vaulted-shopper.md) | GET | Retrieves a vaulted shopper from BlueSnap. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Vaulted Shopper](actions/create-vaulted-shopper.md) | POST | Creates a vaulted shopper in BlueSnap. |
| [Delete Vaulted Shopper](actions/delete-vaulted-shopper.md) | DELETE | Deletes a vaulted shopper from BlueSnap. |
| [List Vaulted Shoppers](actions/list-vaulted-shoppers.md) | GET | Retrieves vaulted shoppers from BlueSnap. |
| [Update Vaulted Shopper](actions/update-vaulted-shopper.md) | PUT | Updates a vaulted shopper in BlueSnap. |

### Refunds

| Action | Method | Description |
| --- | --- | --- |
| [Refund Transaction](actions/refund-transaction.md) | POST | Creates a refund for a BlueSnap transaction. |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Create Plan](actions/create-plan.md) | POST | Creates a plan in BlueSnap. |
| [List Plans](actions/list-plans.md) | GET | Retrieves plans from BlueSnap. |
| [Retrieve Plan](actions/retrieve-plan.md) | GET | Retrieves a plan from BlueSnap. |
| [Update Plan](actions/update-plan.md) | PUT | Updates a plan in BlueSnap. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a subscription in BlueSnap. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from BlueSnap. |
| [Retrieve Subscription](actions/retrieve-subscription.md) | GET | Retrieves a subscription from BlueSnap. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates a subscription in BlueSnap. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Capture Authorized Transaction](actions/capture-authorized-transaction.md) | PUT | Captures an authorized BlueSnap transaction. |
| [Create Transaction](actions/create-transaction.md) | POST | Creates a transaction in BlueSnap. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from BlueSnap. |
| [Retrieve Transaction](actions/retrieve-transaction.md) | GET | Retrieves a transaction from BlueSnap. |
| [Reverse Authorized Transaction](actions/reverse-authorized-transaction.md) | PUT | Reverses an authorized BlueSnap transaction. |

