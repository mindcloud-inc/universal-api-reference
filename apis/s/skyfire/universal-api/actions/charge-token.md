# Skyfire: Charge Token

Creates a new token charge in Skyfire.

```
POST https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/charge-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/charge-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "token": "eyJhbGciOi..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/charge-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "token": "eyJhbGciOi..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `token` | string | yes | The complete, signed JWT string received from the buyer agent in your API call. Example: `eyJhbGciOi...`. |
| `chargeAmount` | string | no | The amount to charge from the token. Example: `0.01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountCharged": "string",
      "remainingBalance": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountCharged` | string |  |
| `remainingBalance` | string |  |

## Native endpoint

Through the native Skyfire API, this operation is `POST /tokens/charge` (base URL `https://api.skyfire.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/charge-token.md) for the provider-specific parameters and requirements.

