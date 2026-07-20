# Grok: Create Client Secret

Creates a realtime client secret in Grok.

```
POST https://connect.mindcloud.co/v1/universal/grok/latest/actions/create-client-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grok/latest/actions/create-client-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/create-client-secret', {
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
| `expiresAfter.seconds` | number | no | Seconds until the client secret expires. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresAt": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | number | Unix timestamp when the client secret expires. |
| `value` | string | Realtime client secret value. |

## Native endpoint

Through the native Grok API, this operation is `POST /v1/realtime/client_secrets` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client-secret.md) for the provider-specific parameters and requirements.

