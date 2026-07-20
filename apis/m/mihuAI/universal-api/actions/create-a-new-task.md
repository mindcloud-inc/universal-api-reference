# Mihu AI: Create a New Task



```
POST https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/create-a-new-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/create-a-new-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentUuid": "string",
  "scheduledAt": "string",
  "title": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/create-a-new-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentUuid": "string",
    "scheduledAt": "string",
    "title": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentUuid` | string | yes |  |
| `autoQueue` | boolean | no |  |
| `campaignUuid` | string | no |  |
| `contactUuid` | string | no |  |
| `description` | string | no |  |
| `priority` | number | no |  |
| `scheduledAt` | string | yes |  |
| `timezone` | string | no |  |
| `title` | string | yes |  |
| `type` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentUuid": "string",
      "autoQueue": true,
      "campaignUuid": "string",
      "contactUuid": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "priority": 1,
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "timezone": "string",
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentUuid` | string |  |
| `autoQueue` | boolean |  |
| `campaignUuid` | string |  |
| `contactUuid` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `priority` | number |  |
| `scheduledAt` | date |  |
| `status` | string |  |
| `timezone` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mihu AI API, this operation is `POST /api/v1/tasks` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-task.md) for the provider-specific parameters and requirements.

