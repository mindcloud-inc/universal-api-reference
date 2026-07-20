# Priority Matrix: Create Project Webhook

Creates a webhook for a Priority Matrix project.

```
POST https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/create-project-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/create-project-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "string",
  "target": "string",
  "project": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/create-project-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "string",
    "target": "string",
    "project": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | yes | Webhook event, for example item.created. |
| `target` | string | yes | Webhook delivery URL. |
| `project` | string | yes | Project resource URI, for example /api/v1/project/234/. |

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

Through the native Priority Matrix API, this operation is `POST /api/v1/hook/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-webhook.md) for the provider-specific parameters and requirements.

