# <img src="https://images.mindcloud.co/apps/icons/images_1773960184395.png" alt="Easyship logo" width="28" height="28"> Easyship: Universal API

Easyship shipping and logistics platform for rates, shipments, pickups, tracking, shipping rules, and fulfillment operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easyship/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.easyship.com
- **Vendor API docs:** https://developers.easyship.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Information](actions/get-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET | Retrieves current account information from Easyship. |

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Address](actions/create-address.md) | POST | Creates a new address in Easyship. |
| [List Addresses](actions/list-addresses.md) | GET | Retrieves a list of addresses from Easyship. |
| [Update Address](actions/update-address.md) | PUT | Updates an existing address in Easyship. |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch of Labels](actions/create-batch-of-labels.md) | POST | Creates a batch of shipment labels in Easyship. |

### Courier

| Action | Method | Description |
| --- | --- | --- |
| [List Couriers](actions/list-couriers.md) | GET | Retrieves a list of couriers from Easyship. |

### Courier Service

| Action | Method | Description |
| --- | --- | --- |
| [List Courier Services](actions/list-courier-services.md) | GET | Retrieves a list of courier services from Easyship. |

### Pickup

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Pickup](actions/cancel-pickup.md) | PUT | Cancels a pickup in Easyship. |
| [Create Pickup](actions/create-pickup.md) | POST | Creates a new pickup in Easyship. |
| [List Pickups](actions/list-pickups.md) | GET | Retrieves a list of pickups from Easyship. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Easyship. |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from Easyship. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Easyship. |

### Rate

| Action | Method | Description |
| --- | --- | --- |
| [Request Rates](actions/request-rates.md) | GET | Retrieves shipping rates from Easyship. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Shipment](actions/cancel-shipment.md) | PUT | Cancels a shipment in Easyship. |
| [Create Shipment](actions/create-shipment.md) | POST | Creates a new shipment in Easyship. |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment from Easyship. |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves a list of shipments from Easyship. |
| [Update Shipment](actions/update-shipment.md) | PUT | Updates an existing shipment in Easyship. |

### Shipmenttracking

| Action | Method | Description |
| --- | --- | --- |
| [List Shipment Trackings](actions/list-shipment-trackings.md) | GET | Retrieves shipment tracking history from Easyship. |

### Shippingrule

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipping Rule](actions/create-shipping-rule.md) | POST | Creates a new shipping rule in Easyship. |
| [Get Shipping Rule](actions/get-shipping-rule.md) | GET | Retrieves a shipping rule from Easyship. |
| [List Shipping Rules](actions/list-shipping-rules.md) | GET | Retrieves a list of shipping rules from Easyship. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from Easyship. |

