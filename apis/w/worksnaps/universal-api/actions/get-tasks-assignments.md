# Worksnaps: Get tasks assignments

Retrieves task assignments from a Worksnaps project.

```
GET https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-tasks-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-tasks-assignments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-tasks-assignments?${params}`, {
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
| `project_id` | string | no | ID of the target project |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "project_id": 1,
      "task_id": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | the ID of the task assignment |
| `project_id` | number | the ID of the project |
| `task_id` | number | the Id of the task |
| `user_id` | number | the ID of the user |

## Native endpoint

Through the native Worksnaps API, this operation is `GET /projects/{project_id}/task_assignments.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tasks-assignments.md) for the provider-specific parameters and requirements.

