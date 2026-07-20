# YouCan: Order Statuses

Retrieves custom order statuses from YouCan.

```
GET https://connect.mindcloud.co/v1/universal/youCan/latest/actions/order-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/order-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youCan/latest/actions/order-statuses?${params}`, {
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
      "ordersStatus": [
        {
          "color": "string",
          "name": "Ava Chen",
          "slug": "string",
          "type": "string"
        }
      ],
      "payment": [
        {
          "color": "string",
          "name": "Ava Chen",
          "slug": "string",
          "type": "string"
        }
      ],
      "shipping": [
        {
          "color": "string",
          "name": "Ava Chen",
          "slug": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ordersStatus` | array<object> |  |
| `ordersStatus[].color` | string |  |
| `ordersStatus[].name` | string |  |
| `ordersStatus[].slug` | string |  |
| `ordersStatus[].type` | string |  |
| `payment` | array<object> |  |
| `payment[].color` | string |  |
| `payment[].name` | string |  |
| `payment[].slug` | string |  |
| `payment[].type` | string |  |
| `shipping` | array<object> |  |
| `shipping[].color` | string |  |
| `shipping[].name` | string |  |
| `shipping[].slug` | string |  |
| `shipping[].type` | string |  |

## Native endpoint

Through the native YouCan API, this operation is `GET /orders/settings` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/order-statuses.md) for the provider-specific parameters and requirements.

