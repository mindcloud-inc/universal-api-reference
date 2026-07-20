# Hex: Cancel Project Run



```
DELETE https://connect.mindcloud.co/v1/universal/hex/latest/actions/cancel-project-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hex/latest/actions/cancel-project-run?connectionId=$CONNECTION_ID&projectId=string&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hex/latest/actions/cancel-project-run?${params}`, {
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
| `projectId` | string | yes | Unique ID for a Hex project. |
| `runId` | string | yes | Unique ID for a Hex project run. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Hex API returns.

## Native endpoint

Through the native Hex API, this operation is `DELETE /projects/:projectId/runs/:runId` (base URL `https://app.hex.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-project-run.md) for the provider-specific parameters and requirements.

