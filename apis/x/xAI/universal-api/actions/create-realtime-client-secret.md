# xAI: Create Realtime Client Secret

Creates a realtime client secret in the xAI API.

```
POST https://connect.mindcloud.co/v1/universal/xAI/latest/actions/create-realtime-client-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/create-realtime-client-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xAI/latest/actions/create-realtime-client-secret', {
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
| `expires_after` | object | no | Expiration object for the ephemeral client secret. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires_at": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires_at` | number |  |
| `value` | string |  |

## Native endpoint

Through the native xAI API, this operation is `POST /realtime/client_secrets` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-realtime-client-secret.md) for the provider-specific parameters and requirements.

