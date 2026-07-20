# Toodledo: Create Tasks

Creates tasks in Toodledo.

```
POST https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-tasks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tasks": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-tasks', {
  method: 'POST',
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
| `tasks` | string | yes | JSON-encoded array of up to 50 task objects. Each task object must include a title. |
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
      "ref": "string",
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
| `ref` | string | Client correlation reference. |
| `star` | number | Starred flag. |
| `title` | string | Task title. |

## Native endpoint

Through the native Toodledo API, this operation is `POST /tasks/add.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tasks.md) for the provider-specific parameters and requirements.

