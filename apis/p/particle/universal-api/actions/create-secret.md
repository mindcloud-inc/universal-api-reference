# Particle: Create Secret



```
POST https://connect.mindcloud.co/v1/universal/particle/latest/actions/create-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/particle/latest/actions/create-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "secret.name": "Ava Chen",
  "secret.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/create-secret', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "secret.name": "Ava Chen",
    "secret.value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `secret.name` | string | yes |  |
| `secret.value` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "secretName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `secretName` | string |  |

## Native endpoint

Through the native Particle API, this operation is `POST /v1/secrets` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-secret.md) for the provider-specific parameters and requirements.

