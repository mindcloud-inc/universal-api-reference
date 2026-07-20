# BugHerd: Create Webhook

Creates a new webhook in BugHerd.

```
POST https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "target_url": "https://example.com/bugherd-webhook",
  "event": "task_create"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "target_url": "https://example.com/bugherd-webhook",
    "event": "task_create"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | number | no | Example: `511891`. |
| `target_url` | string | yes | Example: `https://example.com/bugherd-webhook`. |
| `event` | string | yes | Example: `task_create`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCount": {},
      "event": "string",
      "firstErrorAt": {},
      "firstSuccessAt": {},
      "id": 1,
      "lastErrorAt": {},
      "lastErrorCode": {},
      "lastSuccessAt": {},
      "projectId": 1,
      "projectName": "Ava Chen",
      "successCount": {},
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCount` | object |  |
| `event` | string |  |
| `firstErrorAt` | object |  |
| `firstSuccessAt` | object |  |
| `id` | number |  |
| `lastErrorAt` | object |  |
| `lastErrorCode` | object |  |
| `lastSuccessAt` | object |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `successCount` | object |  |
| `targetUrl` | string |  |

## Native endpoint

Through the native BugHerd API, this operation is `POST webhooks.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

