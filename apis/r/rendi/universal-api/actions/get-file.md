# Rendi: Get File

Retrieves a stored file from Rendi.

```
GET https://connect.mindcloud.co/v1/universal/rendi/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rendi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rendi/latest/actions/get-file?connectionId=$CONNECTION_ID&fileId=86bb48ca-9f6d-4eff-b5a1-e8b426f169ac" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "86bb48ca-9f6d-4eff-b5a1-e8b426f169ac"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rendi/latest/actions/get-file?${params}`, {
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
| `fileId` | string | yes | UUID of the stored file. Example: `86bb48ca-9f6d-4eff-b5a1-e8b426f169ac`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codec": "string",
      "duration": 1,
      "file_format": "string",
      "file_id": "string",
      "file_type": "string",
      "height": 1,
      "is_deleted": true,
      "mime_type": "string",
      "original_file_url": "https://example.com",
      "pixel_format": "string",
      "rendi_store_type": "string",
      "size_mbytes": 1,
      "status": "string",
      "storage_url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codec` | string | Detected codec when available. |
| `duration` | number | Media duration in seconds when available. |
| `file_format` | string | Detected file format. |
| `file_id` | string | Unique file identifier. |
| `file_type` | string | Media type classification. |
| `height` | number | Media height in pixels when available. |
| `is_deleted` | boolean | Deletion flag for the stored file. |
| `mime_type` | string | MIME type for the file. |
| `original_file_url` | string | Original file name or source URL. |
| `pixel_format` | string | Pixel format when available. |
| `rendi_store_type` | string | Storage category for the file. |
| `size_mbytes` | number | Stored file size in MB. |
| `status` | string | Current file status. |
| `storage_url` | string | Direct URL to the stored file. |
| `width` | number | Media width in pixels when available. |

## Native endpoint

Through the native Rendi API, this operation is `GET /v1/files/:file_id` (base URL `https://api.rendi.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

