# eBay: Get Inventory Item



```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-inventory-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-inventory-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-inventory-item?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sku` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": {
        "shipToLocationAvailability": {
          "allocationByFormat": {
            "auction": 1,
            "fixedPrice": 1
          },
          "quantity": 1
        }
      },
      "condition": "string",
      "conditionDescription": "string",
      "locale": "string",
      "product": {
        "brand": "string",
        "description": "string",
        "imageUrls": [
          "https://example.com"
        ],
        "mpn": "string",
        "subtitle": "string",
        "title": "string"
      },
      "sku": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability.shipToLocationAvailability.allocationByFormat.auction` | number |  |
| `availability.shipToLocationAvailability.allocationByFormat.fixedPrice` | number |  |
| `availability.shipToLocationAvailability.quantity` | number |  |
| `condition` | string |  |
| `conditionDescription` | string |  |
| `locale` | string |  |
| `product.brand` | string |  |
| `product.description` | string |  |
| `product.imageUrls[]` | string |  |
| `product.mpn` | string |  |
| `product.subtitle` | string |  |
| `product.title` | string |  |
| `sku` | string |  |

## Native endpoint

Through the native eBay API, this operation is `GET sell/inventory/v1/inventory_item/:sku` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-item.md) for the provider-specific parameters and requirements.

