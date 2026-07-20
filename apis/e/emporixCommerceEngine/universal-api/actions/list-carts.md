# Emporix Commerce Engine: List Carts

Retrieves carts from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-carts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-carts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-carts?${params}`, {
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
      "calculatedPrice": {},
      "currency": "string",
      "customerId": "string",
      "id": "string",
      "items": [
        {}
      ],
      "legalEntityId": "string",
      "metadata": {},
      "orderId": "string",
      "quoteId": "string",
      "siteCode": "string",
      "totalPrice": {},
      "totalUnitsCount": 1,
      "type": "string",
      "yrn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calculatedPrice` | object |  |
| `currency` | string |  |
| `customerId` | string |  |
| `id` | string |  |
| `items` | array<object> |  |
| `legalEntityId` | string |  |
| `metadata` | object |  |
| `orderId` | string |  |
| `quoteId` | string |  |
| `siteCode` | string |  |
| `totalPrice` | object |  |
| `totalUnitsCount` | number |  |
| `type` | string |  |
| `yrn` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /cart/{{credentials.tenantId}}/carts` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-carts.md) for the provider-specific parameters and requirements.

