# CircleCI: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[]": [
    "string"
  ],
  "name": "Ava Chen",
  "scope": {},
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[]": ["string"],
    "name": "Ava Chen",
    "scope": {},
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[]` | array<string> | yes | Events that should trigger this webhook. |
| `name` | string | yes | Webhook display name. |
| `scope` | object | yes | Webhook scope configuration. |
| `signing_secret` | string | no | Secret used to sign webhook payloads. |
| `url` | string | yes | Destination URL for webhook deliveries. |
| `verify_tls` | boolean | no | Whether CircleCI should verify the server certificate. |

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

Through the native CircleCI API, this operation is `POST /webhook` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

