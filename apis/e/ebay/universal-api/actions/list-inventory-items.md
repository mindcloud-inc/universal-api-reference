# eBay: List Inventory Items



```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-inventory-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-inventory-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-inventory-items?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": {
        "shipToLocationAvailability": {
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

Through the native eBay API, this operation is `GET sell/inventory/v1/inventory_item` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory-items.md) for the provider-specific parameters and requirements.

