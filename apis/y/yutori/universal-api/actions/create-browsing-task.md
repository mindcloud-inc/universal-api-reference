# Yutori: Create Browsing Task

Creates a Yutori browsing task for an automated web workflow.

```
POST https://connect.mindcloud.co/v1/universal/yutori/latest/actions/create-browsing-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yutori `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yutori/latest/actions/create-browsing-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task": "string",
  "startUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yutori/latest/actions/create-browsing-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task": "string",
    "startUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task` | string | yes |  |
| `startUrl` | string | yes |  |
| `maxSteps` | number | no |  |
| `requireAuth` | boolean | no |  |
| `outputSchema` | object | no |  |
| `webhookUrl` | string | no |  |
| `webhookFormat` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "task_id": "string",
      "view_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `task_id` | string |  |
| `view_url` | string |  |

## Native endpoint

Through the native Yutori API, this operation is `POST /v1/browsing/tasks` (base URL `https://api.yutori.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-browsing-task.md) for the provider-specific parameters and requirements.

