# Emporix Commerce Engine: List Prices

Retrieves prices from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-prices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-prices?${params}`, {
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
      "currency": "string",
      "id": "string",
      "itemYrn": "string",
      "metadata": {},
      "mixins": {},
      "priceModelId": "string",
      "salePrice": {},
      "tierValues": [
        {}
      ],
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `id` | string |  |
| `itemYrn` | string |  |
| `metadata` | object |  |
| `mixins` | object |  |
| `priceModelId` | string |  |
| `salePrice` | object |  |
| `tierValues` | array<object> |  |
| `vendorId` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /price/{{credentials.tenantId}}/prices` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-prices.md) for the provider-specific parameters and requirements.

