# Automate Team - Task Management: Get Task Counts



```
GET https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/get-task-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Automate Team - Task Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/get-task-counts?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/get-task-counts?${params}`, {
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
| `workspaceId` | number | yes | Numeric workspace id, for example 33371. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed_count": 1,
      "completed_in_time_count": 1,
      "delayed_count": 1,
      "in_progress_count": 1,
      "overdue_count": 1,
      "pending_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed_count` | number |  |
| `completed_in_time_count` | number |  |
| `delayed_count` | number |  |
| `in_progress_count` | number |  |
| `overdue_count` | number |  |
| `pending_count` | number |  |

## Native endpoint

Through the native Automate Team - Task Management API, this operation is `POST /rest/v1/rpc/get_task_counts_v52_cc` (base URL `https://api.automatebusiness.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-counts.md) for the provider-specific parameters and requirements.

