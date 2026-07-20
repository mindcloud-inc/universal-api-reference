# Mihu AI: Delete a Task



```
DELETE https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/delete-a-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/delete-a-task?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/delete-a-task?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes |  |

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

Through the native Mihu AI API, this operation is `DELETE /api/v1/tasks/:uuid` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-task.md) for the provider-specific parameters and requirements.

