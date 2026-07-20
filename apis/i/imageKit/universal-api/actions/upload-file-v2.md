# ImageKit.io: Upload File V2

Uploads a file to ImageKit.io using Upload API v2.

```
POST https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/upload-file-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageKit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/upload-file-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "https://yavuzceliker.github.io/sample-images/image-1021.jpg",
  "fileName": "codex-upload-v2.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/upload-file-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "https://yavuzceliker.github.io/sample-images/image-1021.jpg",
    "fileName": "codex-upload-v2.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes | Default: `https://yavuzceliker.github.io/sample-images/image-1021.jpg`. |
| `fileName` | string | yes | Default: `codex-upload-v2.jpg`. |
| `folder` | string | no | Default: `codex-uploads`. |
| `useUniqueFileName` | boolean | no |  |
| `isPrivateFile` | boolean | no |  |
| `tags` | list<string> | no | Accepts multiple values as an array. |
| `customCoordinates` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `responseFields` | list<string> | no | Accepts multiple values as an array. |
| `webhookUrl` | string | no |  |
| `overwriteFile` | boolean | no |  |
| `overwriteAITags` | boolean | no |  |
| `overwriteTags` | boolean | no |  |
| `overwriteCustomMetadata` | boolean | no |  |
| `customMetadata` | string | no |  |
| `extensions` | string | no |  |
| `transformation` | string | no |  |
| `checks` | string | no |  |
| `token` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiTags": [
        "string"
      ],
      "description": "string",
      "fileId": "string",
      "filePath": "string",
      "fileType": "string",
      "height": 1,
      "name": "Ava Chen",
      "size": 1,
      "thumbnailUrl": "https://example.com",
      "url": "https://example.com",
      "versionInfo": {},
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiTags` | array<string> |  |
| `description` | string |  |
| `fileId` | string |  |
| `filePath` | string |  |
| `fileType` | string |  |
| `height` | number |  |
| `name` | string |  |
| `size` | number |  |
| `thumbnailUrl` | string |  |
| `url` | string |  |
| `versionInfo` | object |  |
| `width` | number |  |

## Native endpoint

Through the native ImageKit.io API, this operation is `POST https://upload.imagekit.io/api/v2/files/upload` (base URL `https://api.imagekit.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-v2.md) for the provider-specific parameters and requirements.

