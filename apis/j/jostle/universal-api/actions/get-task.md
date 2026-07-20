# Jostle: Get Task



```
GET https://connect.mindcloud.co/v1/universal/jostle/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jostle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jostle/latest/actions/get-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jostle/latest/actions/get-task?${params}`, {
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
| `id` | string | yes | Id of the task |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": {
        "username": "Ava Chen"
      },
      "collaborators": {
        "users": [
          {
            "username": "Ava Chen"
          }
        ]
      },
      "commentCount": 1,
      "completedTime": {},
      "completionStatus": true,
      "description": {},
      "dueDate": {},
      "taskState": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee.username` | string |  |
| `collaborators.users[].username` | string |  |
| `commentCount` | number |  |
| `completedTime` | object |  |
| `completionStatus` | boolean |  |
| `description` | object |  |
| `dueDate` | object |  |
| `taskState` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Jostle API, this operation is `GET /v2/tasks/task/:id` (base URL `https://api-prod.jostle.us`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

