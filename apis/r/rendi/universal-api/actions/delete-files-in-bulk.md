# Rendi: Delete Files in Bulk

Deletes multiple stored files from Rendi.

```
DELETE https://connect.mindcloud.co/v1/universal/rendi/latest/actions/delete-files-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rendi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rendi/latest/actions/delete-files-in-bulk?connectionId=$CONNECTION_ID&fileIds=987fcdeb-a89b-43d3-b456-789012345678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileIds": "987fcdeb-a89b-43d3-b456-789012345678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rendi/latest/actions/delete-files-in-bulk?${params}`, {
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
| `fileIds` | object<string> | yes | Array of file UUIDs to delete (1-1000 items). Example: `987fcdeb-a89b-43d3-b456-789012345678`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted_file_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted_file_ids` | array<string> | List of file UUIDs that were successfully deleted |

## Native endpoint

Through the native Rendi API, this operation is `POST /v1/files/bulk-delete` (base URL `https://api.rendi.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-files-in-bulk.md) for the provider-specific parameters and requirements.

