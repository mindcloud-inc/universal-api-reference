# Moorcheh: Delete File

Deletes files from a Moorcheh namespace in storage.

```
DELETE https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moorcheh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/delete-file?connectionId=$CONNECTION_ID&namespace_name=Ava%20Chen&file_name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "namespace_name": "Ava Chen",
  "file_name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/delete-file?${params}`, {
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
| `namespace_name` | string | yes | Namespace that contains the file or files. |
| `file_name` | string | yes | Single file to permanently delete, such as document.pdf. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_names[]` | array<string> | no | Multiple file names to permanently delete in one request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "namespace": "Ava Chen",
      "results": [
        {
          "file_name": "Ava Chen",
          "message": "string",
          "status": "string"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Human-readable deletion message. |
| `namespace` | string | Namespace where files were deleted. |
| `results` | array<object> | Per-file deletion results. |
| `results[].file_name` | string | File name processed. |
| `results[].message` | string | Per-file result message. |
| `results[].status` | string | Per-file status, such as deleted or error. |
| `success` | boolean | Whether the delete request completed. |

## Native endpoint

Through the native Moorcheh API, this operation is `DELETE /namespaces/:namespace_name/delete-file` (base URL `https://api.moorcheh.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

