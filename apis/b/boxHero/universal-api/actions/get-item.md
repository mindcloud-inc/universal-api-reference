# BoxHero: Get Item

Retrieves an item from BoxHero.

```
GET https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-item?connectionId=$CONNECTION_ID&itemId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-item?${params}`, {
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
| `itemId` | number | yes | Unique identifier for the item |
| `locationIds[]` | array<number> | no | Use these locations for quantity calculation |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {
        "attrs": [
          {
            "id": 1,
            "name": "Ava Chen",
            "type": "string",
            "value": "string"
          }
        ],
        "barcode": "string",
        "cost": "string",
        "id": 1,
        "name": "Ava Chen",
        "photo_url": "https://example.com",
        "price": "string",
        "quantities": [
          {
            "location_id": 1,
            "quantity": 1
          }
        ],
        "quantity": 1,
        "sku": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item.attrs[].id` | number |  |
| `item.attrs[].name` | string |  |
| `item.attrs[].type` | string |  |
| `item.attrs[].value` | string |  |
| `item.barcode` | string |  |
| `item.cost` | string |  |
| `item.id` | number |  |
| `item.name` | string |  |
| `item.photo_url` | string |  |
| `item.price` | string |  |
| `item.quantities[].location_id` | number |  |
| `item.quantities[].quantity` | number |  |
| `item.quantity` | number |  |
| `item.sku` | string |  |

## Native endpoint

Through the native BoxHero API, this operation is `GET /v1/items/:item_id` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

