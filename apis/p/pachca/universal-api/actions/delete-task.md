# Pachca: Delete task



```
DELETE https://connect.mindcloud.co/v1/universal/pachca/latest/actions/delete-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/delete-task?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachca/latest/actions/delete-task?${params}`, {
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
| `id` | number | yes | Pachca task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | number |  |

## Native endpoint

Through the native Pachca API, this operation is `DELETE /tasks/{id}` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task.md) for the provider-specific parameters and requirements.

