# Viewneo: Upload Media File

Uploads a media file to Viewneo.

```
POST https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/upload-media-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewneo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/upload-media-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaFileIdAsParentDirectory": 1,
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/upload-media-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaFileIdAsParentDirectory": 1,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaFileIdAsParentDirectory` | number | yes | ID of folder |
| `file` | file | yes | File to upload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachable": {
        "colorMode": 1,
        "companyId": 1,
        "convertedFileHash": "string",
        "createdAt": "string",
        "deletedAt": {},
        "duration": {},
        "extension": "string",
        "fileHash": "string",
        "fileSize": 1,
        "height": 1,
        "id": 1,
        "info": {},
        "mimeType": "string",
        "originalExtension": "string",
        "originalName": "Ava Chen",
        "pixabayId": {},
        "status": 1,
        "updatedAt": "string",
        "width": 1
      },
      "attachableId": 1,
      "attachableType": "string",
      "companyId": 1,
      "createdAt": "string",
      "deletedAt": {},
      "id": 1,
      "isDefault": 1,
      "isDemo": 1,
      "isHidden": 1,
      "isLocked": 1,
      "isShared": 1,
      "mediaFileIdAsParentDirectory": 1,
      "name": "Ava Chen",
      "status": 1,
      "thumbnailExtension": "string",
      "thumbnailHash": "string",
      "thumbnailMimeType": "string",
      "type": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachable.colorMode` | number |  |
| `attachable.companyId` | number |  |
| `attachable.convertedFileHash` | string |  |
| `attachable.createdAt` | string |  |
| `attachable.deletedAt` | object |  |
| `attachable.duration` | object |  |
| `attachable.extension` | string |  |
| `attachable.fileHash` | string |  |
| `attachable.fileSize` | number |  |
| `attachable.height` | number |  |
| `attachable.id` | number |  |
| `attachable.info` | object |  |
| `attachable.mimeType` | string |  |
| `attachable.originalExtension` | string |  |
| `attachable.originalName` | string |  |
| `attachable.pixabayId` | object |  |
| `attachable.status` | number |  |
| `attachable.updatedAt` | string |  |
| `attachable.width` | number |  |
| `attachableId` | number |  |
| `attachableType` | string |  |
| `companyId` | number |  |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `id` | number |  |
| `isDefault` | number |  |
| `isDemo` | number |  |
| `isHidden` | number |  |
| `isLocked` | number |  |
| `isShared` | number |  |
| `mediaFileIdAsParentDirectory` | number |  |
| `name` | string |  |
| `status` | number |  |
| `thumbnailExtension` | string |  |
| `thumbnailHash` | string |  |
| `thumbnailMimeType` | string |  |
| `type` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Viewneo API, this operation is `POST /mediafile` (base URL `https://cloud.viewneo.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-media-file.md) for the provider-specific parameters and requirements.

