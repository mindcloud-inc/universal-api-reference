# Flexport: List Products

Retrieves products for a client from Flexport.

```
GET https://connect.mindcloud.co/v1/universal/flexport/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexport `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexport/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexport/latest/actions/list-products?${params}`, {
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
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "classifications": [
        {}
      ],
      "clientVerified": true,
      "countryOfOrigin": "string",
      "description": "string",
      "hsCodes": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "productCategory": "string",
      "productProperties": [
        {}
      ],
      "sku": "string",
      "suppliers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | date |  |
| `classifications` | array<object> |  |
| `clientVerified` | boolean |  |
| `countryOfOrigin` | string |  |
| `description` | string |  |
| `hsCodes` | array<object> |  |
| `id` | number |  |
| `name` | string |  |
| `productCategory` | string |  |
| `productProperties` | array<object> |  |
| `sku` | string |  |
| `suppliers` | array<object> |  |

## Native endpoint

Through the native Flexport API, this operation is `GET /products` (base URL `https://api.flexport.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

