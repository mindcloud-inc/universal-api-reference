# Emporix Commerce Engine: Search Carts

Finds carts in Emporix Commerce Engine by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/search-carts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/search-carts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/search-carts?${params}`, {
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
      "status": "string",
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
| `status` | string |  |
| `totalUnitsCount` | number |  |
| `type` | string |  |
| `yrn` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `POST /cart/{{credentials.tenantId}}/carts/search` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-carts.md) for the provider-specific parameters and requirements.

