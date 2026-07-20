# <img src="https://images.mindcloud.co/apps/icons/shipcloud-1_1777385404155.png" alt="Shipcloud logo" width="28" height="28"> Shipcloud: Universal API

Create shipments, manifests, pickup requests, trackers, addresses, orders, shipment documents, and webhooks in Shipcloud.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shipcloud/latest
- **Category:** Commerce
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shipcloud.io/
- **Vendor API docs:** https://developers.shipcloud.io/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Address](actions/create-address.md) | POST | Creates a new address in Shipcloud. |
| [Get Address](actions/get-address.md) | GET | Retrieves an address from Shipcloud by ID. |
| [Get Default Returns Address](actions/get-default-returns-address.md) | GET | Retrieves the default returns address from Shipcloud. |
| [Get Default Shipping Address](actions/get-default-shipping-address.md) | GET | Retrieves the default shipping address from Shipcloud. |
| [Get Invoice Address](actions/get-invoice-address.md) | GET | Retrieves the invoice address from Shipcloud. |
| [List Addresses](actions/list-addresses.md) | GET | Retrieves addresses from Shipcloud. |

### Carrier

| Action | Method | Description |
| --- | --- | --- |
| [List Carriers](actions/list-carriers.md) | GET | Retrieves carriers from Shipcloud. |

### Manifest

| Action | Method | Description |
| --- | --- | --- |
| [Create Manifest](actions/create-manifest.md) | POST | Creates a new manifest in Shipcloud. |
| [Get Manifest](actions/get-manifest.md) | GET | Retrieves a manifest from Shipcloud by ID. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Shipcloud. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Shipcloud by ID. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Shipcloud. |

### Pickup Dropoff Location

| Action | Method | Description |
| --- | --- | --- |
| [Search Pickup Dropoff Locations](actions/search-pickup-dropoff-locations.md) | GET | Finds pickup dropoff locations in Shipcloud. |

### Pickup Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Pickup Request](actions/create-pickup-request.md) | POST | Creates a new pickup request in Shipcloud. |
| [Get Pickup Request](actions/get-pickup-request.md) | GET | Retrieves a pickup request from Shipcloud by ID. |
| [List Pickup Requests](actions/list-pickup-requests.md) | GET | Retrieves pickup requests from Shipcloud. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment](actions/create-shipment.md) | POST | Creates a new shipment in Shipcloud. |
| [Delete Shipment](actions/delete-shipment.md) | DELETE | Deletes an existing shipment from Shipcloud. |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment from Shipcloud by ID. |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves shipments from Shipcloud. |
| [Update Shipment](actions/update-shipment.md) | PUT | Updates an existing shipment in Shipcloud. |

### Shipment Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment Document](actions/create-shipment-document.md) | POST | Creates a new shipment document in Shipcloud. |
| [Get Shipment Document](actions/get-shipment-document.md) | GET | Retrieves a shipment document from Shipcloud by ID. |
| [List Shipment Documents](actions/list-shipment-documents.md) | GET | Retrieves shipment documents from Shipcloud. |

### Shipment Quote

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment Quote](actions/create-shipment-quote.md) | POST | Creates a new shipment quote in Shipcloud. |

### Tracker

| Action | Method | Description |
| --- | --- | --- |
| [Create Tracker](actions/create-tracker.md) | POST | Creates a new tracker in Shipcloud. |
| [Get Tracker](actions/get-tracker.md) | GET | Retrieves a tracker from Shipcloud by ID. |
| [List Trackers](actions/list-trackers.md) | GET | Retrieves trackers from Shipcloud. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Shipcloud. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Shipcloud. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Shipcloud. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Shipcloud by ID. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Shipcloud. |

