# Particle: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/particle/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/particle/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "mindcloud-test-webhook",
  "integration_type": "Webhook",
  "requestType": "POST",
  "url": "https://httpbin.org/post"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "mindcloud-test-webhook",
    "integration_type": "Webhook",
    "requestType": "POST",
    "url": "https://httpbin.org/post"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | yes | Default: `mindcloud-test-webhook`. |
| `integration_type` | string | yes | Default: `Webhook`. |
| `name` | string | no |  |
| `requestType` | string | yes | Default: `POST`. |
| `url` | string | yes | Default: `https://httpbin.org/post`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": "string",
      "id": "string",
      "integrationType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event` | string |  |
| `id` | string |  |
| `integrationType` | string |  |

## Native endpoint

Through the native Particle API, this operation is `POST /v1/integrations` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

