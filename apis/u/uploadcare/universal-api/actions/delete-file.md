# Uploadcare: Delete File

Deletes an existing file from Uploadcare storage.

```
DELETE https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/delete-file?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/delete-file?${params}`, {
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
| `uuid` | string | yes | Uploadcare file UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentInfo": {},
      "datetimeRemoved": "2026-05-07T12:00:00.000Z",
      "datetimeStored": "2026-05-07T12:00:00.000Z",
      "datetimeUploaded": "2026-05-07T12:00:00.000Z",
      "isImage": true,
      "isReady": true,
      "metadata": {},
      "mimeType": "string",
      "originalFilename": "Ava Chen",
      "originalFileUrl": "https://example.com",
      "size": 1,
      "url": "https://example.com",
      "uuid": "string",
      "variations": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentInfo` | object | Detected content information. |
| `datetimeRemoved` | date | Timestamp when the file was removed. |
| `datetimeStored` | date | Timestamp when the file was stored. |
| `datetimeUploaded` | date | Timestamp when the file was uploaded. |
| `isImage` | boolean | Whether the file is an image. |
| `isReady` | boolean | Whether the file is ready for delivery. |
| `metadata` | object | Custom metadata map. |
| `mimeType` | string | Detected MIME type. |
| `originalFilename` | string | Original uploaded filename. |
| `originalFileUrl` | string | Original CDN file URL. |
| `size` | number | File size in bytes. |
| `url` | string | REST API URL for the file. |
| `uuid` | string | Uploadcare file UUID. |
| `variations` | object | Available file variations when present. |

## Native endpoint

Through the native Uploadcare API, this operation is `DELETE /files/:uuid/storage/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

