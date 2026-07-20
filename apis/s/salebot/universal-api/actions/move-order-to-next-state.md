# Salebot: Move Order to Next State



```
PUT https://connect.mindcloud.co/v1/universal/salebot/latest/actions/move-order-to-next-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/move-order-to-next-state" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1,
  "orderId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salebot/latest/actions/move-order-to-next-state', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1,
    "orderId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | yes | Existing Salebot client ID. |
| `orderId` | number | yes | Existing Salebot order ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "stateId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stateId` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Salebot API, this operation is `POST /move_order_to_next_state` (base URL `https://chatter.salebot.pro/api/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-order-to-next-state.md) for the provider-specific parameters and requirements.

