# RO App: Update Order Status



```
PUT https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-order-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-order-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": 1,
  "statusId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-order-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": 1,
    "statusId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | yes | Order ID |
| `statusId` | number | yes | Status ID |
| `comment` | string | no | Status comment |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "comment": "string",
      "group": {
        "name": "Ava Chen",
        "type": 1
      },
      "id": 1,
      "name": "Ava Chen",
      "status_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `comment` | string |  |
| `group` | object |  |
| `group.name` | string |  |
| `group.type` | number |  |
| `id` | number |  |
| `name` | string |  |
| `status_id` | number |  |

## Native endpoint

Through the native RO App API, this operation is `POST /orders/:order_id/status` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order-status.md) for the provider-specific parameters and requirements.

