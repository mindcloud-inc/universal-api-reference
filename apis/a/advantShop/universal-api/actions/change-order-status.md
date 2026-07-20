# AdvantShop: Change Order Status

Updates an order status in AdvantShop.

```
PUT https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/change-order-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AdvantShop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/change-order-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": 1,
  "statusId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/change-order-status', {
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
| `orderId` | number | yes | Order identifier to update. |
| `statusId` | number | yes | Target order status identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "result": true,
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `result` | boolean |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native AdvantShop API, this operation is `POST /order/changestatus` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-order-status.md) for the provider-specific parameters and requirements.

