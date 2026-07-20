# Biyo POS: List Products

Retrieves product records from Biyo POS.

```
GET https://connect.mindcloud.co/v1/universal/biyoPOS/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Biyo POS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biyoPOS/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/biyoPOS/latest/actions/list-products?${params}`, {
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
      "archived": true,
      "barcode": "string",
      "categories": [
        {}
      ],
      "color": "string",
      "cost": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "price": 1,
      "storeStockInfo": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `barcode` | string |  |
| `categories` | array<object> |  |
| `color` | string |  |
| `cost` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `price` | number |  |
| `storeStockInfo` | array<object> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Biyo POS API, this operation is `GET /api/v1/products/` (base URL `https://mindcloud.biyo.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

