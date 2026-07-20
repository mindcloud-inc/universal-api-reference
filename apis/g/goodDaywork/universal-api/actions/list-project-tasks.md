# GoodDay.work: List Project Tasks

Finds tasks in a GoodDay.work project.

```
GET https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-project-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-project-tasks?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-project-tasks?${params}`, {
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
| `projectId` | string | yes | GoodDay project ID. |
| `closed` | boolean | no | Include closed tasks. |
| `subfolders` | boolean | no | Include tasks from subfolders. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToUserId": "string",
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToUserId` | string | Assigned user ID. |
| `id` | string | Task ID. |
| `name` | string | Task title. |
| `projectId` | string | Associated project ID. |
| `status` | object | Task status object. |

## Native endpoint

Through the native GoodDay.work API, this operation is `GET /project/:projectId/tasks` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-tasks.md) for the provider-specific parameters and requirements.

