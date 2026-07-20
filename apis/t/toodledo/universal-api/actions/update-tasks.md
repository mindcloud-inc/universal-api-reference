# Toodledo: Update Tasks

Updates existing tasks in Toodledo.

```
PUT https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/update-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/update-tasks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tasks": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/update-tasks', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tasks": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tasks` | string | yes | JSON-encoded array of up to 50 task objects. Each task object must include an id. |
| `reschedule` | number | no | Set to 1 to let Toodledo reschedule repeating tasks automatically when completion is provided. |
| `fields` | string | no | Comma-separated optional task fields to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": 1,
      "folder": 1,
      "id": 1,
      "modified": 1,
      "star": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | number | Completion timestamp or 0. |
| `folder` | number | Folder ID. |
| `id` | number | Task ID. |
| `modified` | number | Last modification timestamp. |
| `star` | number | Starred flag. |
| `title` | string | Task title. |

## Native endpoint

Through the native Toodledo API, this operation is `POST /tasks/edit.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tasks.md) for the provider-specific parameters and requirements.

