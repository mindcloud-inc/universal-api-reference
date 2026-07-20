# Knack: Upload File Image Asset



```
POST https://connect.mindcloud.co/v1/universal/knack/latest/actions/upload-file-image-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Knack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/knack/latest/actions/upload-file-image-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assetType": "file",
  "files": "https://www.w3.org/TR/PNG/iso_8859-1.txt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/knack/latest/actions/upload-file-image-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assetType": "file",
    "files": "https://www.w3.org/TR/PNG/iso_8859-1.txt"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assetType` | string | yes | Upload target type: file or image. Example: `file`. |
| `files` | file | yes | Remote URL, base64, or binary content for the file or image to upload. Example: `https://www.w3.org/TR/PNG/iso_8859-1.txt`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "id": "string",
      "public_url": "https://example.com",
      "size": 1,
      "thumb_url": "https://example.com",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string |  |
| `id` | string |  |
| `public_url` | string |  |
| `size` | number |  |
| `thumb_url` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Knack API, this operation is `POST /applications/{{credentials.applicationId}}/assets/:asset_type/upload` (base URL `https://api.knack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-image-asset.md) for the provider-specific parameters and requirements.

