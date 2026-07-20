# BugHerd: List User Tasks

Retrieves tasks for a BugHerd user.

```
GET https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-user-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-user-tasks?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-user-tasks?${params}`, {
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
| `userId` | number | yes | The BugHerd user ID. |
| `updatedSince` | string | no | Return tasks updated after this timestamp. |
| `createdSince` | string | no | Return tasks created after this timestamp. |
| `priority` | string | no | Filter tasks by BugHerd priority. |
| `tag` | string | no | Filter tasks by tag. |
| `assignedToId` | number | no | Filter tasks assigned to a specific user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "userTasks": [
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
| `id` | number |  |
| `name` | string |  |
| `userTasks` | array<object> |  |

## Native endpoint

Through the native BugHerd API, this operation is `GET users/:user_id/tasks.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-tasks.md) for the provider-specific parameters and requirements.

