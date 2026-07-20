# ProjectManager: Retrieve TaskTags

Retrieves task tags from ProjectManager.

```
GET https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-task-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-task-tags?connectionId=$CONNECTION_ID&taskId=22222222-2222-2222-2222-222222222222" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "22222222-2222-2222-2222-222222222222"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-task-tags?${params}`, {
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
| `taskId` | string | yes | The unique identifier of the Task for which we will retrieve TaskTags Example: `22222222-2222-2222-2222-222222222222`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `GET /api/data/tasks/:taskId/tags` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-task-tags.md) for the provider-specific parameters and requirements.

