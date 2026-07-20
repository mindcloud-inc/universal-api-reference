# Port API AI: Create Webhook

Creates a webhook in Port.

```
POST https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "title": "string",
  "mappings[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "title": "string",
    "mappings[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | The webhook identifier. |
| `title` | string | yes | The webhook title. |
| `enabled` | boolean | no | Whether the webhook is enabled. |
| `mappings[]` | array<object> | yes | Webhook mappings configuration. |
| `security` | object | no | Webhook security configuration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "integration": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `integration` | object |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /webhooks` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

