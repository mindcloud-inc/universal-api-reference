# Nozbe Teams: List Task Events

Retrieves accessible task events from Nozbe Teams.

```
GET https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-task-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-task-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-task-events?${params}`, {
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
| `taskId` | string | no | Return only events for this task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "change": "string",
      "createdAt": 1,
      "id": "string",
      "integration": "string",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `change` | string |  |
| `createdAt` | number |  |
| `id` | string |  |
| `integration` | string |  |
| `taskId` | string |  |

## Native endpoint

Through the native Nozbe Teams API, this operation is `GET /task_events` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-events.md) for the provider-specific parameters and requirements.

