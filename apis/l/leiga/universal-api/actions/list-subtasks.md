# Leiga: List Subtasks

Retrieves subtasks from Leiga for an issue.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-subtasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-subtasks?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-subtasks?${params}`, {
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
| `id` | number | yes | Parent Issue ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualLabour": 1,
      "assigneeId": 1,
      "assigneeName": "Ava Chen",
      "createTime": 1,
      "done": true,
      "dueDate": 1,
      "estimateLabour": 1,
      "estimatePoint": 1,
      "id": 1,
      "issueNumber": 1,
      "remainingLabour": 1,
      "startDate": 1,
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualLabour` | number | Actual labour. |
| `assigneeId` | number | Assignee ID. |
| `assigneeName` | string | Assignee name. |
| `createTime` | number | Creation timestamp. |
| `done` | boolean | Whether the subtask is done. |
| `dueDate` | number | Due timestamp. |
| `estimateLabour` | number | Estimated labour. |
| `estimatePoint` | number | Estimate points. |
| `id` | number | Subtask ID. |
| `issueNumber` | number | Subtask number. |
| `remainingLabour` | number | Remaining labour. |
| `startDate` | number | Start timestamp. |
| `summary` | string | Subtask summary. |

## Native endpoint

Through the native Leiga API, this operation is `POST /issue/list-subtask` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subtasks.md) for the provider-specific parameters and requirements.

