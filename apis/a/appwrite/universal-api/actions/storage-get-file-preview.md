# Appwrite: Get file preview

Retrieves the file preview from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-get-file-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-get-file-preview?connectionId=$CONNECTION_ID&bucketId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucketId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-get-file-preview?${params}`, {
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
| `bucketId` | string | yes | Storage bucket unique ID. You can create a new storage bucket using the Storage service [server integration](https://appwrite.io/docs/server/storage#createBucket). |
| `fileId` | string | yes | File ID |
| `width` | number | no | Resize preview image width, Pass an integer between 0 to 4000. |
| `height` | number | no | Resize preview image height, Pass an integer between 0 to 4000. |
| `gravity` | string | no | Image crop gravity. Can be one of center,top-left,top,top-right,left,right,bottom-left,bottom,bottom-right |
| `quality` | number | no | Preview image quality. Pass an integer between 0 to 100. Defaults to keep existing image quality. |
| `borderWidth` | number | no | Preview image border in pixels. Pass an integer between 0 to 100. Defaults to 0. |
| `borderColor` | string | no | Preview image border color. Use a valid HEX color, no # is needed for prefix. |
| `borderRadius` | number | no | Preview image border radius in pixels. Pass an integer between 0 to 4000. |
| `opacity` | number | no | Preview image opacity. Only works with images having an alpha channel (like png). Pass a number between 0 to 1. |
| `rotation` | number | no | Preview image rotation in degrees. Pass an integer between -360 and 360. |
| `background` | string | no | Preview image background color. Only works with transparent images (png). Use a valid HEX color, no # is needed for prefix. |
| `output` | string | no | Output format type (jpeg, jpg, png, gif and webp). |
| `token` | string | no | File token for accessing this file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object | Provider response payload. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /storage/buckets/{bucketId}/files/{fileId}/preview` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/storage-get-file-preview.md) for the provider-specific parameters and requirements.

