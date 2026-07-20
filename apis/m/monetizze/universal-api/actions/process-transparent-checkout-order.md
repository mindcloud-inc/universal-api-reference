# Monetizze: Process Transparent Checkout Order

Creates a transparent checkout order in Monetizze.

```
POST https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/process-transparent-checkout-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monetizze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/process-transparent-checkout-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/process-transparent-checkout-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | object | yes | Full Monetizze transparent checkout processing JSON object as documented for this endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string | Transparent checkout processing message returned by Monetizze. |
| `status` | number | Transparent checkout processing status returned by Monetizze. |

## Native endpoint

Through the native Monetizze API, this operation is `POST https://app.monetizze.com.br/checkout/transparente/processar` (base URL `https://api.monetizze.com.br/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-transparent-checkout-order.md) for the provider-specific parameters and requirements.

