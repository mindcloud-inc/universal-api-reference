# STEL Order: List Products

Retrieves a list of products from STEL Order.

```
GET https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STEL Order `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-products?${params}`, {
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
      "barcode": "string",
      "composite": true,
      "deleted": true,
      "description": "string",
      "id": 1,
      "inactive": true,
      "location": {},
      "name": "Ava Chen",
      "path": "string",
      "promotional": true,
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `barcode` | string |  |
| `composite` | boolean |  |
| `deleted` | boolean |  |
| `description` | string |  |
| `id` | number |  |
| `inactive` | boolean |  |
| `location` | object |  |
| `name` | string |  |
| `path` | string |  |
| `promotional` | boolean |  |
| `reference` | string |  |

## Native endpoint

Through the native STEL Order API, this operation is `GET /products` (base URL `https://app.stelorder.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

