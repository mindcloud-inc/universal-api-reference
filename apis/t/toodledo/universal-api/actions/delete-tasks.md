# Toodledo: Delete Tasks

Deletes existing tasks from Toodledo.

```
DELETE https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/delete-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/delete-tasks?connectionId=$CONNECTION_ID&tasks=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tasks": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/delete-tasks?${params}`, {
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
| `tasks` | string | yes | JSON-encoded array of up to 50 task IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Deleted task ID. |

## Native endpoint

Through the native Toodledo API, this operation is `POST /tasks/delete.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tasks.md) for the provider-specific parameters and requirements.

