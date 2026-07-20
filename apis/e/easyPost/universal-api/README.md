# <img src="https://images.mindcloud.co/apps/icons/easy-post_1776100177828.png" alt="EasyPost logo" width="28" height="28"> EasyPost: Universal API

EasyPost provides shipping APIs for rates, labels, tracking, customs, pickups, batches, refunds, and related shipping operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easyPost/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.easypost.com
- **Vendor API docs:** https://docs.easypost.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Shipments](actions/list-shipments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Address](actions/create-address.md) | POST | Creates a new address in EasyPost. |
| [Create And Verify Address](actions/create-and-verify-address.md) | POST | Creates and verifies a new address in EasyPost. |
| [Get Address](actions/get-address.md) | GET | Retrieves details for an address from EasyPost. |
| [List Addresses](actions/list-addresses.md) | GET | Retrieves a list of addresses from EasyPost. |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Add Shipments To Batch](actions/add-shipments-to-batch.md) | PUT | Adds shipments to an existing batch in EasyPost. |
| [Buy Batch](actions/buy-batch.md) | PUT | Purchases an existing batch in EasyPost. |
| [Create Batch](actions/create-batch.md) | POST | Creates a new batch in EasyPost. |
| [Get Batch](actions/get-batch.md) | GET | Retrieves details for a batch from EasyPost. |
| [List Batches](actions/list-batches.md) | GET | Retrieves a list of batches from EasyPost. |
| [Remove Shipments From Batch](actions/remove-shipments-from-batch.md) | PUT | Removes shipments from an existing batch in EasyPost. |

### Batch Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch Label](actions/create-batch-label.md) | PUT | Creates a label for an existing batch in EasyPost. |

### Batch Scan Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch Scan Form](actions/create-batch-scan-form.md) | PUT | Creates a scan form for an existing batch in EasyPost. |

### Customs Info

| Action | Method | Description |
| --- | --- | --- |
| [Create Customs Info](actions/create-customs-info.md) | POST | Creates new customs info in EasyPost. |
| [Get Customs Info](actions/get-customs-info.md) | GET | Retrieves details for customs info from EasyPost. |

### Customs Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Customs Item](actions/create-customs-item.md) | POST | Creates a new customs item in EasyPost. |
| [Get Customs Item](actions/get-customs-item.md) | GET | Retrieves details for a customs item from EasyPost. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Buy Order](actions/buy-order.md) | PUT | Purchases an existing order in EasyPost. |
| [Create Order](actions/create-order.md) | POST | Creates a new order in EasyPost. |
| [Get Order](actions/get-order.md) | GET | Retrieves details for an order from EasyPost. |

### Parcel

| Action | Method | Description |
| --- | --- | --- |
| [Create Parcel](actions/create-parcel.md) | POST | Creates a new parcel in EasyPost. |
| [Get Parcel](actions/get-parcel.md) | GET | Retrieves details for a parcel from EasyPost. |

### Pickup

| Action | Method | Description |
| --- | --- | --- |
| [Buy Pickup](actions/buy-pickup.md) | PUT | Purchases an existing pickup in EasyPost. |
| [Cancel Pickup](actions/cancel-pickup.md) | PUT | Cancels an existing pickup in EasyPost. |
| [Create Pickup](actions/create-pickup.md) | POST | Creates a new pickup in EasyPost. |
| [Get Pickup](actions/get-pickup.md) | GET | Retrieves details for a pickup from EasyPost. |
| [List Pickups](actions/list-pickups.md) | GET | Retrieves a list of pickups from EasyPost. |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [Create Refund](actions/create-refund.md) | POST | Creates a new refund in EasyPost. |
| [Get Refund](actions/get-refund.md) | GET | Retrieves details for a refund from EasyPost. |
| [List Refunds](actions/list-refunds.md) | GET | Retrieves a list of refunds from EasyPost. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Buy Shipment](actions/buy-shipment.md) | PUT | Purchases an existing shipment in EasyPost. |
| [Create Shipment](actions/create-shipment.md) | POST | Creates a new shipment in EasyPost. |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves details for a shipment from EasyPost. |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves a list of shipments from EasyPost. |

### Shipment Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment Form](actions/create-shipment-form.md) | POST | Creates a new shipment form in EasyPost. |

### Shipment Insurance

| Action | Method | Description |
| --- | --- | --- |
| [Insure Shipment](actions/insure-shipment.md) | PUT | Creates shipping insurance for a shipment in EasyPost. |

### Shipment Label

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipment Label](actions/get-shipment-label.md) | GET | Retrieves a label for a shipment from EasyPost. |

### Shipment Rate

| Action | Method | Description |
| --- | --- | --- |
| [Rerate Shipment](actions/rerate-shipment.md) | PUT | Refreshes rates for an existing shipment in EasyPost. |

### Tracker

| Action | Method | Description |
| --- | --- | --- |
| [Create Tracker](actions/create-tracker.md) | POST | Creates a new tracker in EasyPost. |
| [Get Tracker](actions/get-tracker.md) | GET | Retrieves details for a tracker from EasyPost. |
| [List Trackers](actions/list-trackers.md) | GET | Retrieves a list of trackers from EasyPost. |

