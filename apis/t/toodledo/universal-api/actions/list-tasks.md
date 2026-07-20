# Toodledo: List Tasks

Retrieves tasks from Toodledo.

```
GET https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-tasks?${params}`, {
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
| `before` | number | no | Return only tasks modified before this GMT Unix timestamp. |
| `after` | number | no | Return only tasks modified after this GMT Unix timestamp. |
| `comp` | number | no | Use 0 for uncompleted only, 1 for completed only, or -1 for both. |
| `id` | number | no | Fetch a single task by its numeric Toodledo task ID. |
| `start` | number | no | Number of records to skip before returning results. |
| `num` | number | no | Maximum number of tasks to return. Toodledo documents a default and max of 1000. |
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
      "priority": 1,
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
| `priority` | number | Priority value. |
| `star` | number | Starred flag. |
| `title` | string | Task title. |

## Native endpoint

Through the native Toodledo API, this operation is `GET /tasks/get.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

