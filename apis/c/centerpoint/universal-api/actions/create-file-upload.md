# Centerpoint: Create File Upload



```
POST https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceFile": "string",
  "subjectType": "companies",
  "subjectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-file-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceFile": "string",
    "subjectType": "companies",
    "subjectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Original filename sent to Centerpoint. |
| `sourceFile` | file | yes | File content. The action converts bare base64 to Centerpoint's required data URI format before sending. |
| `subjectType` | list<string> | yes | Centerpoint subject type for the file attachment. One of: `companies`, `productions`, `properties`. Default: `companies`. |
| `subjectId` | string | yes | Centerpoint subject id to attach the uploaded file to. For company attachments, use the Centerpoint company id. |
| `tags[]` | array<string> | no | Centerpoint model file tags, for example ["Photos"]. |
| `thumbnailSize` | number | no | Thumbnail size for image uploads. Centerpoint examples use 390. Default: `390`. |
| `title` | string | no | Display title for the Centerpoint file. |
| `description` | string | no | Optional file description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "createdAt": "string",
      "createdById": 1,
      "height": 1,
      "id": 1,
      "importId": {},
      "latitude": 1,
      "longitude": 1,
      "mimeType": "string",
      "path": "string",
      "thumbnailPath": "string",
      "thumbnailUrl": "https://example.com",
      "title": "string",
      "type": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `createdAt` | string |  |
| `createdById` | number |  |
| `height` | number |  |
| `id` | number | Centerpoint file ID. |
| `importId` | object |  |
| `latitude` | number | Latitude associated with the file when Centerpoint returns one. |
| `longitude` | number | Longitude associated with the file when Centerpoint returns one. |
| `mimeType` | string |  |
| `path` | string |  |
| `thumbnailPath` | string |  |
| `thumbnailUrl` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Centerpoint API, this operation is `POST file/url` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file-upload.md) for the provider-specific parameters and requirements.

