# Chaser: Create Task

Creates a new task in Chaser.

```
POST https://connect.mindcloud.co/v1/universal/chaser/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chaser/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "summary": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chaser/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "summary": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `summary` | string | yes | Task summary text. |
| `assignee` | string | no | Assignee email address or Slack user group handle. Multiple assignees can be comma-separated. |
| `dueAt` | date | no | Due date in YYYY-MM-DD format. |
| `dueTime` | string | no | Optional due time in HH:mm format using the task creator timezone. Example: `21:30`. |
| `channel` | string | no | Optional Slack channel name. Omit to create the task in the creator's direct-message context. Example: `general`. |
| `multiAssignStrategy` | string | no | Optional strategy for multiple assignees: volunteer or round_robin. One of: `0`, `1`, `2`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chaser API returns.

## Native endpoint

Through the native Chaser API, this operation is `POST /webhooks/tasks` (base URL `https://slack.chaseforme.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

