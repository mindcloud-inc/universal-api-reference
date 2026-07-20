# Emporix Commerce Engine: Search Sales Orders

Finds sales orders in Emporix Commerce Engine by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/search-sales-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/search-sales-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/search-sales-orders?${params}`, {
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
      "cartId": "string",
      "countryCode": "string",
      "currency": "string",
      "customer": {},
      "entries": [
        {}
      ],
      "id": "string",
      "metadata": {},
      "orderType": "string",
      "quoteId": "string",
      "siteCode": "string",
      "status": "string",
      "subTotalPrice": 1,
      "totalAuthorizedAmount": 1,
      "totalPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calculatedPrice` | object |  |
| `cartId` | string |  |
| `countryCode` | string |  |
| `currency` | string |  |
| `customer` | object |  |
| `entries` | array<object> |  |
| `id` | string |  |
| `metadata` | object |  |
| `orderType` | string |  |
| `quoteId` | string |  |
| `siteCode` | string |  |
| `status` | string |  |
| `subTotalPrice` | number |  |
| `totalAuthorizedAmount` | number |  |
| `totalPrice` | number |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `POST /order-v2/{{credentials.tenantId}}/salesorders/search` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-sales-orders.md) for the provider-specific parameters and requirements.

