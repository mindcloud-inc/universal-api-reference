# Zeplin: Update Project Webhook

Updates an existing project webhook in Zeplin.

```
PUT https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-project-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-project-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "webhookId": "string",
  "url": "https://example.com",
  "name": "Ava Chen",
  "secret": "string",
  "status": "string",
  "events[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-project-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "webhookId": "string",
    "url": "https://example.com",
    "name": "Ava Chen",
    "secret": "string",
    "status": "string",
    "events[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project id |
| `webhookId` | string | yes | Webhook id |
| `url` | string | yes | The URL of the webhook |
| `name` | string | yes | The name of the webhook |
| `secret` | string | yes | The secret to be used to generate signatures for webhook requests |
| `status` | string | yes | The status of the webhook |
| `events[]` | array<string> | yes | The events of the webhook |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zeplin API returns.

## Native endpoint

Through the native Zeplin API, this operation is `PATCH /projects/{project_id}/webhooks/{webhook_id}` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-webhook.md) for the provider-specific parameters and requirements.

