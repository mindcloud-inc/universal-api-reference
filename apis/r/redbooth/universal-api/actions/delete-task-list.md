# Redbooth: Delete Task List

Deletes an existing task list from Redbooth.

```
DELETE https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/delete-task-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Redbooth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/delete-task-list?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/delete-task-list?${params}`, {
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
| `id` | number | yes | Redbooth task list ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "retry_after": 1,
      "status": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `retry_after` | number |  |
| `status` | string |  |
| `token` | string |  |

## Native endpoint

Through the native Redbooth API, this operation is `DELETE /task_lists/:id` (base URL `https://redbooth.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task-list.md) for the provider-specific parameters and requirements.

