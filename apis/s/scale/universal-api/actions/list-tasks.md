# Scale: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/scale/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scale/latest/actions/list-tasks?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scale/latest/actions/list-tasks?${params}`, {
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
| `batchId` | string | no | Optional batch identifier filter. |
| `batchName` | string | no | Optional batch name filter. |
| `completedAfter` | string | no | Only return tasks completed after this timestamp. |
| `completedBefore` | string | no | Only return tasks completed before this timestamp. |
| `expand` | string | no | Comma-separated fields to expand in the response. |
| `fields` | string | no | Comma-separated properties to include in the task response. |
| `limit` | string | no | Limit the number of tasks returned. |
| `pageToken` | string | no | Pagination token for the next page. |
| `projectId` | string | yes | Scale project identifier. Required in MindCloud for this action. |
| `projectName` | string | no | Optional alternative to Project ID when you want to scope by project name instead. |
| `status` | string | no | Optional task status filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tasks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tasks` | array<object> | Array of task objects. |

## Native endpoint

Through the native Scale API, this operation is `GET /v2/tasks` (base URL `https://api.scale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

