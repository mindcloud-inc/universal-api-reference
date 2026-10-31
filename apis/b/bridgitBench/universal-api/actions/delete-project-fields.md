# Bridgit Bench: Delete Project Fields



```
DELETE https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/delete-project-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/delete-project-fields?connectionId=$CONNECTION_ID&id=1&payload%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "payload[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/delete-project-fields?${params}`, {
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
| `id` | number | yes | The Account ID |
| `payload[]` | array<number> | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `DELETE /rp/api/v1/accounts/:id/project-fields` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project-fields.md) for the provider-specific parameters and requirements.

