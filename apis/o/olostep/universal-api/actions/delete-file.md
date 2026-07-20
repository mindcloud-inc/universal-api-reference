# Olostep: Delete File

Deletes an existing file from Olostep.

```
DELETE https://connect.mindcloud.co/v1/universal/olostep/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/delete-file?connectionId=$CONNECTION_ID&fileId=file_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "file_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olostep/latest/actions/delete-file?${params}`, {
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
| `fileId` | string | yes | The ID of the file to delete. Example: `file_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the file was deleted. |
| `id` | string | The deleted file ID. |
| `object` | string | The returned object type. |

## Native endpoint

Through the native Olostep API, this operation is `DELETE /v1/files/[:file_id]` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

