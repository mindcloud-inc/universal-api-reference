# PixelBin.io: Get File By ID

Retrieves a file from PixelBin.io by internal ID.

```
GET https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-file-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-file-by-id?connectionId=$CONNECTION_ID&_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-file-by-id?${params}`, {
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
| `_id` | string | yes | PixelBin file _id returned by List Files. |

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
      "name": "Ava Chen",
      "path": "string",
      "size": 1,
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | PixelBin asset identifier. |
| `access` | string | Asset access level. |
| `fileId` | string | Combined file path and name. |
| `format` | string | Asset file format. |
| `name` | string | Asset name. |
| `path` | string | Containing folder path. |
| `size` | number | Asset size in bytes. |
| `type` | string | Returned resource type. |
| `url` | string | PixelBin CDN URL. |

## Native endpoint

Through the native PixelBin.io API, this operation is `GET /service/platform/assets/v1.0/files/id/:_id` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-by-id.md) for the provider-specific parameters and requirements.

