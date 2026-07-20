# Gridly: Delete View

Deletes an existing view from Gridly.

```
DELETE https://connect.mindcloud.co/v1/universal/gridly/latest/actions/delete-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/delete-view?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridly/latest/actions/delete-view?${params}`, {
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
| `id` | string | yes | The unique identifier of the view to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gridly API returns.

## Native endpoint

Through the native Gridly API, this operation is `DELETE /views/:id` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-view.md) for the provider-specific parameters and requirements.

