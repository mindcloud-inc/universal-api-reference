# ImageKit.io: List File Versions

Retrieves all file versions from ImageKit.io.

```
GET https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/list-file-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageKit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/list-file-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/list-file-versions?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "embeddedMetadata": {
        "dateCreated": "2026-05-07T12:00:00.000Z",
        "dateTimeCreated": "2026-05-07T12:00:00.000Z"
      },
      "fileId": "string",
      "filePath": "string",
      "fileType": "string",
      "hasAlpha": true,
      "height": 1,
      "isPrivateFile": true,
      "isPublished": true,
      "mime": "string",
      "name": "Ava Chen",
      "size": 1,
      "thumbnail": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "versionInfo": {
        "id": "string",
        "name": "Ava Chen"
      },
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `embeddedMetadata.dateCreated` | date |  |
| `embeddedMetadata.dateTimeCreated` | date |  |
| `fileId` | string |  |
| `filePath` | string |  |
| `fileType` | string |  |
| `hasAlpha` | boolean |  |
| `height` | number |  |
| `isPrivateFile` | boolean |  |
| `isPublished` | boolean |  |
| `mime` | string |  |
| `name` | string |  |
| `size` | number |  |
| `thumbnail` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `versionInfo.id` | string |  |
| `versionInfo.name` | string |  |
| `width` | number |  |

## Native endpoint

Through the native ImageKit.io API, this operation is `GET /files/:fileId/versions` (base URL `https://api.imagekit.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-file-versions.md) for the provider-specific parameters and requirements.

