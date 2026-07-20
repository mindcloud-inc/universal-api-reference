# ImageKit.io: Get Uploaded File Metadata

Retrieves uploaded file metadata from ImageKit.io.

```
GET https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/get-uploaded-file-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageKit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/get-uploaded-file-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/get-uploaded-file-metadata?${params}`, {
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
| `fileId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "density": 1,
      "format": "string",
      "hasColorProfile": true,
      "hasTransparency": true,
      "height": 1,
      "pHash": "string",
      "quality": 1,
      "size": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `density` | number |  |
| `format` | string |  |
| `hasColorProfile` | boolean |  |
| `hasTransparency` | boolean |  |
| `height` | number |  |
| `pHash` | string |  |
| `quality` | number |  |
| `size` | number |  |
| `width` | number |  |

## Native endpoint

Through the native ImageKit.io API, this operation is `GET /files/:fileId/metadata` (base URL `https://api.imagekit.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-uploaded-file-metadata.md) for the provider-specific parameters and requirements.

