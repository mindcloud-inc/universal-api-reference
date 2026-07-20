# Emporix Commerce Engine: Get Sales Order

Retrieves a sales order from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-sales-order?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-sales-order?${params}`, {
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
| `orderId` | string | yes | The unique ID of the sales order. |

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

Through the native Emporix Commerce Engine API, this operation is `GET /order-v2/{{credentials.tenantId}}/salesorders/:orderId` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-order.md) for the provider-specific parameters and requirements.

