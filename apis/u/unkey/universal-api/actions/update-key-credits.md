# Unkey: Update key credits

Updates credits for an existing API key in Unkey.

```
PUT https://connect.mindcloud.co/v1/universal/unkey/latest/actions/update-key-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/update-key-credits" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keyId": "string",
  "operation": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unkey/latest/actions/update-key-credits', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keyId": "string",
    "operation": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `keyId` | string | yes |  |
| `operation` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "refill": {
          "amount": 1,
          "interval": "string",
          "refillDay": 1
        },
        "remaining": 1
      },
      "meta": {
        "requestId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.refill` | object |  |
| `data.refill.amount` | number |  |
| `data.refill.interval` | string |  |
| `data.refill.refillDay` | number |  |
| `data.remaining` | number |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/keys.updateCredits` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-key-credits.md) for the provider-specific parameters and requirements.

