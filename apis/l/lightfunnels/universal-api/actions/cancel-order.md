# Lightfunnels: Cancel Order



```
DELETE https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/cancel-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/cancel-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/cancel-order?${params}`, {
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
      "cancelOrder": {
        "cancelled": true,
        "cancelledAt": "string",
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelOrder` | object | Cancelled order. |
| `cancelOrder.cancelled` | boolean | Whether the order is cancelled. |
| `cancelOrder.cancelledAt` | string | Cancellation timestamp. |
| `cancelOrder.id` | string | Order id. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-order.md) for the provider-specific parameters and requirements.

