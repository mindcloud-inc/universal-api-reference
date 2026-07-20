# Rye: Create Payment Gateway Session

Creates a payment gateway session in Rye.

```
POST https://connect.mindcloud.co/v1/universal/rye/latest/actions/create-payment-gateway-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rye `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rye/latest/actions/create-payment-gateway-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "gateway": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rye/latest/actions/create-payment-gateway-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "gateway": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `gateway` | string | yes | The payment gateway to create a session for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "container": "string",
      "gateway": "string",
      "sessionKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `container` | string |  |
| `gateway` | string |  |
| `sessionKey` | string |  |

## Native endpoint

Through the native Rye API, this operation is `POST /api/v1/payment-gateways/{gateway}/session` (base URL `https://staging.api.rye.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-gateway-session.md) for the provider-specific parameters and requirements.

