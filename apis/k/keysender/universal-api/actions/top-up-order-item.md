# Keysender: Top Up Order Item

Creates a top-up for a Keysender order item.

```
POST https://connect.mindcloud.co/v1/universal/keysender/latest/actions/top-up-order-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keysender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/top-up-order-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keysender/latest/actions/top-up-order-item', {
  method: 'POST',
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
| `iccid` | string | no |  |
| `orderId` | string | no |  |
| `topUpSku` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "iccid": "string",
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
| `iccid` | string | ICCID associated with the top-up. |
| `message` | string | Top-up result message. |
| `status` | string | Top-up status. |

## Native endpoint

Through the native Keysender API, this operation is `POST /catalog/order/top-up` (base URL `https://panel.keysender.co.uk/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/top-up-order-item.md) for the provider-specific parameters and requirements.

