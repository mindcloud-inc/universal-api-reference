# Xano: Delete Table Record

Deletes an existing record from a Xano table.

```
DELETE https://connect.mindcloud.co/v1/universal/xano/latest/actions/delete-table-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xano/latest/actions/delete-table-record?connectionId=$CONNECTION_ID&content_id=1&table_id=1&workspace_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "content_id": "1",
  "table_id": "1",
  "workspace_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xano/latest/actions/delete-table-record?${params}`, {
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
| `content_id` | number | yes |  |
| `table_id` | number | yes |  |
| `workspace_id` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Xano API returns.

## Native endpoint

Through the native Xano API, this operation is `DELETE /api%3Ameta/workspace/:workspace_id/table/:table_id/content/:content_id` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-table-record.md) for the provider-specific parameters and requirements.

