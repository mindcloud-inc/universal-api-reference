# PixelBin.io: Upload Asset From URL

Creates a new uploaded file in PixelBin.io from a URL.

```
POST https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/url-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/url-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/url-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `access` | string | no | Access level for the uploaded asset. |
| `filenameOverride` | boolean | no | Whether to append a unique suffix when a matching file name already exists. |
| `metadata` | object | no | Metadata object to associate with the upload. |
| `name` | string | no | Name for the uploaded asset. |
| `overwrite` | boolean | no | Whether to overwrite an existing asset with the same name. |
| `path` | string | no | Path where the uploaded asset should be stored. |
| `tags[]` | array<string> | no | Tags to associate with the upload. |
| `url` | string | yes | Source URL for the asset to upload into PixelBin. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "access": "string",
      "fileId": "string",
      "format": "string",
      "metadata": {},
      "name": "Ava Chen",
      "path": "string",
      "size": 1,
      "tags": [
        "string"
      ],
      "thumbnail": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | PixelBin file record ID. |
| `access` | string | Asset access level. |
| `fileId` | string | Combined PixelBin file path and name. |
| `format` | string | File format. |
| `metadata` | object | Metadata associated with the uploaded file. |
| `name` | string | File name. |
| `path` | string | Containing folder path. |
| `size` | number | File size in bytes. |
| `tags` | array<string> | Tags associated with the uploaded file. |
| `thumbnail` | string | Thumbnail URL when PixelBin provides one. |
| `url` | string | PixelBin CDN URL for the file. |

## Native endpoint

Through the native PixelBin.io API, this operation is `POST /service/platform/assets/v1.0/upload/url` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/url-upload.md) for the provider-specific parameters and requirements.

