# Chaser: List Tasks

Retrieves tasks from Chaser.

```
GET https://connect.mindcloud.co/v1/universal/chaser/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chaser/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chaser/latest/actions/list-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "tasks": [
        {
          "assignees": [
            "string"
          ],
          "channelId": "string",
          "completedAt": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "dueDate": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "link": "https://example.com",
          "status": "string",
          "summary": "string",
          "timezoneId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tasks` | array<object> | All tasks currently visible to the authenticated Chaser workspace. |
| `tasks[].assignees` | array<string> | Slack user ids assigned to the task. |
| `tasks[].channelId` | string | Slack channel or DM id where the task lives. |
| `tasks[].completedAt` | string | Completion date when fully completed; empty otherwise. |
| `tasks[].createdAt` | date | Task creation date. |
| `tasks[].dueDate` | date | Due date in YYYY-MM-DD format. |
| `tasks[].id` | string | Chaser task id. |
| `tasks[].link` | string | Slack permalink for the task thread. |
| `tasks[].status` | string | Task status. Chaser currently documents Not Acknowledged, Acknowledged, or Completed. |
| `tasks[].summary` | string | Task summary. |
| `tasks[].timezoneId` | string | Timezone used for due-time interpretation. |

## Native endpoint

Through the native Chaser API, this operation is `GET /webapi/tasks` (base URL `https://slack.chaseforme.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

