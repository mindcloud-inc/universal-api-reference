# Rendi: Delete File

Deletes a stored file from Rendi.

```
DELETE https://connect.mindcloud.co/v1/universal/rendi/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rendi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rendi/latest/actions/delete-file?connectionId=$CONNECTION_ID&fileId=86bb48ca-9f6d-4eff-b5a1-e8b426f169ac" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "86bb48ca-9f6d-4eff-b5a1-e8b426f169ac"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rendi/latest/actions/delete-file?${params}`, {
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
| `fileId` | string | yes | UUID of the stored file to delete. Example: `86bb48ca-9f6d-4eff-b5a1-e8b426f169ac`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rendi API returns.

## Native endpoint

Through the native Rendi API, this operation is `DELETE /v1/files/:file_id` (base URL `https://api.rendi.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

