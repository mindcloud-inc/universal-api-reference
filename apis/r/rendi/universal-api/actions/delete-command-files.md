# Rendi: Delete Command Files

Deletes stored output files for a command in Rendi.

```
DELETE https://connect.mindcloud.co/v1/universal/rendi/latest/actions/delete-command-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rendi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rendi/latest/actions/delete-command-files?connectionId=$CONNECTION_ID&commandId=5f3f7a72-f14e-4f02-8feb-8debbf29eeac" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commandId": "5f3f7a72-f14e-4f02-8feb-8debbf29eeac"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rendi/latest/actions/delete-command-files?${params}`, {
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
| `commandId` | string | yes | UUID of the command whose stored files should be deleted. Example: `5f3f7a72-f14e-4f02-8feb-8debbf29eeac`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rendi API returns.

## Native endpoint

Through the native Rendi API, this operation is `DELETE /v1/commands/:command_id/files` (base URL `https://api.rendi.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-command-files.md) for the provider-specific parameters and requirements.

