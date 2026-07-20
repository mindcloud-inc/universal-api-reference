# Particle: Test Integration



```
PUT https://connect.mindcloud.co/v1/universal/particle/latest/actions/test-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/particle/latest/actions/test-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "integrationId": "0123456789abcdef01234567"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/test-integration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "integrationId": "0123456789abcdef01234567"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | string | no |  |
| `device_id` | string | no |  |
| `integrationId` | string | yes | Default: `0123456789abcdef01234567`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "pass": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `pass` | boolean |  |

## Native endpoint

Through the native Particle API, this operation is `POST /v1/integrations/:integrationId/test` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-integration.md) for the provider-specific parameters and requirements.

