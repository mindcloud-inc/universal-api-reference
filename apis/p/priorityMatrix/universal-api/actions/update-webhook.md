# Priority Matrix: Update Webhook

Updates an existing webhook in Priority Matrix.

```
PUT https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Priority Matrix webhook ID. |
| `event` | string | no | Webhook event name. |
| `target` | string | no | Webhook target URL. |
| `enabled` | boolean | no | Whether the webhook is enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "event": "string",
      "id": 1,
      "project": "string",
      "resource_uri": "string",
      "target": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `event` | string |  |
| `id` | number |  |
| `project` | string |  |
| `resource_uri` | string |  |
| `target` | string |  |

## Native endpoint

Through the native Priority Matrix API, this operation is `PUT /api/v1/hook/:id/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

