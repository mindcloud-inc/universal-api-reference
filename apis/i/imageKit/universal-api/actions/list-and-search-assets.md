# ImageKit.io: List and Search Assets

Finds files in ImageKit.io with search and filter options.

```
GET https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/list-and-search-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageKit.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/list-and-search-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/list-and-search-assets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "aiTags": [
        "string"
      ],
      "bitRate": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customCoordinates": {},
      "customMetadata": {},
      "duration": 1,
      "embeddedMetadata": {},
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
      "tags": [
        "string"
      ],
      "thumbnail": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "versionInfo": {},
      "videoCodec": "string",
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
| `bitRate` | number |  |
| `createdAt` | date |  |
| `customCoordinates` | object |  |
| `customMetadata` | object |  |
| `duration` | number |  |
| `embeddedMetadata` | object |  |
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
| `tags` | array<string> |  |
| `thumbnail` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `versionInfo` | object |  |
| `videoCodec` | string |  |
| `width` | number |  |

## Native endpoint

Through the native ImageKit.io API, this operation is `GET /files` (base URL `https://api.imagekit.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-and-search-assets.md) for the provider-specific parameters and requirements.

