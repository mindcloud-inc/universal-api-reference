# SmartRoutes: List Orders



```
GET https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartRoutes `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/list-orders?${params}`, {
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
| `status` | string | no | Filter orders by status. |
| `customerId` | number | no | Filter orders by customer ID. |
| `orderNumber` | string | no | Filter orders by order number. |
| `updatedAtMin` | date | no | Minimum updated date and time for filtering. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "customer": {},
      "id": 1,
      "order_number": "string",
      "status": "string",
      "stops": [
        {}
      ],
      "type": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `customer` | object |  |
| `id` | number |  |
| `order_number` | string |  |
| `status` | string |  |
| `stops` | array<object> |  |
| `type` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native SmartRoutes API, this operation is `GET /orders` (base URL `https://api.smartroutes.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

