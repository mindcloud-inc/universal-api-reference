# GoDial: Delete Task

Deletes an existing task from GoDial.

```
DELETE https://connect.mindcloud.co/v1/universal/goDial/latest/actions/task-remove
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/task-remove?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDial/latest/actions/task-remove?${params}`, {
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
| `id` | string | yes | Task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |

## Native endpoint

Through the native GoDial API, this operation is `DELETE /externals/tasks/[:id]/remove` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/task-remove.md) for the provider-specific parameters and requirements.

