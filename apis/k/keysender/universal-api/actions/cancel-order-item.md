# Keysender: Cancel Order Item

Cancels an order item in Keysender.

```
PUT https://connect.mindcloud.co/v1/universal/keysender/latest/actions/cancel-order-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keysender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/cancel-order-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keysender/latest/actions/cancel-order-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `incrementId` | string | no |  |
| `lineItemId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCode` | string | Provider error code when present. |
| `message` | string | Cancellation result message. |
| `status` | string | Cancellation status. |

## Native endpoint

Through the native Keysender API, this operation is `POST /catalog/order/cancel-item` (base URL `https://panel.keysender.co.uk/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-order-item.md) for the provider-specific parameters and requirements.

