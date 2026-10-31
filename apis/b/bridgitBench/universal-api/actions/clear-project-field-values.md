# Bridgit Bench: Clear Project Field Values



```
DELETE https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/clear-project-field-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/clear-project-field-values?connectionId=$CONNECTION_ID&accountId=1&projectId=1&payload%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "projectId": "1",
  "payload[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/clear-project-field-values?${params}`, {
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
| `accountId` | number | yes | The Account ID |
| `projectId` | number | yes | The project ID the role belongs to |
| `payload[]` | array<number> | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/project-field-values` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-project-field-values.md) for the provider-specific parameters and requirements.

