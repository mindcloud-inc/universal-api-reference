# CircleCI: Update Webhook



```
PUT https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhook_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhook_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events` | string | no | Events that should trigger this webhook. |
| `name` | string | no | Webhook display name. |
| `signing_secret` | string | no | Secret used to sign webhook payloads. |
| `url` | string | no | Destination URL for webhook deliveries. |
| `verify_tls` | string | no | Whether CircleCI should verify the server certificate. |
| `webhook_id` | string | yes | Opaque webhook identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "url": "https://example.com",
      "verifyTls": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `url` | string |  |
| `verifyTls` | boolean |  |

## Native endpoint

Through the native CircleCI API, this operation is `PUT /webhook/:webhook_id` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

