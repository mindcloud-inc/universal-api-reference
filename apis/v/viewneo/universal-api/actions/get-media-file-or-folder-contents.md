# Viewneo: Get Media File or Folder Contents

Retrieves a media file or folder contents from Viewneo.

```
GET https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-media-file-or-folder-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewneo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-media-file-or-folder-contents?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-media-file-or-folder-contents?${params}`, {
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
| `id` | number | yes | ID of mediaFile |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachable": {
        "appContentId": {},
        "appDuration": {},
        "appLabel1": {},
        "appLabel2": {},
        "appScope": {},
        "appThumbnailPlaylistEntryUrl": {},
        "appThumbnailUrl": {},
        "companyId": 1,
        "createdAt": "string",
        "deletedAt": {},
        "id": 1,
        "type": 1,
        "updatedAt": "string",
        "url": "https://example.com"
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
      "thumbnailExtension": {},
      "thumbnailHash": {},
      "thumbnailMimeType": {},
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
| `attachable.appContentId` | object |  |
| `attachable.appDuration` | object |  |
| `attachable.appLabel1` | object |  |
| `attachable.appLabel2` | object |  |
| `attachable.appScope` | object |  |
| `attachable.appThumbnailPlaylistEntryUrl` | object |  |
| `attachable.appThumbnailUrl` | object |  |
| `attachable.companyId` | number |  |
| `attachable.createdAt` | string |  |
| `attachable.deletedAt` | object |  |
| `attachable.id` | number |  |
| `attachable.type` | number |  |
| `attachable.updatedAt` | string |  |
| `attachable.url` | string |  |
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
| `thumbnailExtension` | object |  |
| `thumbnailHash` | object |  |
| `thumbnailMimeType` | object |  |
| `type` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Viewneo API, this operation is `GET /mediafile/:id` (base URL `https://cloud.viewneo.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-file-or-folder-contents.md) for the provider-specific parameters and requirements.

