# Xano: Delete API Group

Deletes an existing API group from Xano.

```
DELETE https://connect.mindcloud.co/v1/universal/xano/latest/actions/delete-api-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xano/latest/actions/delete-api-group?connectionId=$CONNECTION_ID&apigroup_id=1&workspace_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apigroup_id": "1",
  "workspace_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xano/latest/actions/delete-api-group?${params}`, {
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
| `apigroup_id` | number | yes | The Xano API group ID. |
| `workspace_id` | number | yes | The Xano workspace ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Xano API returns.

## Native endpoint

Through the native Xano API, this operation is `DELETE /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-api-group.md) for the provider-specific parameters and requirements.

