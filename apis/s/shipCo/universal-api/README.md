# <img src="https://images.mindcloud.co/apps/icons/ship-and-co-icon_1778094575562.png" alt="Ship&Co logo" width="28" height="28"> Ship&Co: Universal API

Ship&Co is a shipping and tracking API for creating labels, managing orders, retrieving rates, registering carriers, tracking shipments, and managing fulfillment addresses and warehouses.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shipCo/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.shipandco.com/en/api
- **Vendor API docs:** https://developer.shipandco.com/en/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Shipments](actions/list-shipments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/list-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Carrier

| Action | Method | Description |
| --- | --- | --- |
| [Delete Carrier](actions/delete-carrier.md) | DELETE |  |
| [List Carriers](actions/list-carriers.md) | GET |  |
| [Register Carrier](actions/register-carrier.md) | POST |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET |  |
| [Upload File](actions/upload-file.md) | POST |  |

### Negotiated Rate

| Action | Method | Description |
| --- | --- | --- |
| [Delete Negotiated Rates](actions/delete-negotiated-rates.md) | DELETE |  |
| [Upload Negotiated Rates](actions/upload-negotiated-rates.md) | PUT |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST |  |
| [Delete Order](actions/delete-order.md) | DELETE |  |
| [List Orders](actions/list-orders.md) | GET |  |

### Rate

| Action | Method | Description |
| --- | --- | --- |
| [List Rates](actions/list-rates.md) | GET |  |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment](actions/create-shipment.md) | POST |  |
| [Delete Shipment](actions/delete-shipment.md) | DELETE |  |
| [Get Shipment](actions/get-shipment.md) | GET |  |
| [List Shipments](actions/list-shipments.md) | GET |  |

### Shipping Address

| Action | Method | Description |
| --- | --- | --- |
| [List Shipping Addresses](actions/list-shipping-addresses.md) | GET |  |
| [Register Shipping Address](actions/register-shipping-address.md) | POST |  |

### Sub User

| Action | Method | Description |
| --- | --- | --- |
| [Delete Sub User](actions/delete-sub-user.md) | DELETE |  |
| [Get Sub User](actions/get-sub-user.md) | GET |  |
| [List Sub Users](actions/list-sub-users.md) | GET |  |
| [Register Sub User](actions/register-sub-user.md) | POST |  |

### Sub User Token

| Action | Method | Description |
| --- | --- | --- |
| [Regenerate Sub User API Token](actions/regenerate-sub-user-api-token.md) | PUT |  |

### Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Get Tracking](actions/get-tracking.md) | GET |  |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [List Warehouses](actions/list-warehouses.md) | GET |  |
| [Register Warehouse](actions/register-warehouse.md) | POST |  |

