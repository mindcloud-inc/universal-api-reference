# Linkbreakers: List Media Files

Retrieves a list of media files from Linkbreakers.

```
GET https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-media-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-media-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-media-files?${params}`, {
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
      "media": [
        {
          "createdAt": "string",
          "fileName": "Ava Chen",
          "id": "string",
          "mediaType": "string",
          "mimeType": "string",
          "signedUrl": "https://example.com",
          "size": "string",
          "updatedAt": "string",
          "uploadedBy": "string",
          "visibility": "string",
          "workspaceId": "string"
        }
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `media` | array<object> | Page of media assets. |
| `media[].createdAt` | string |  |
| `media[].fileName` | string |  |
| `media[].id` | string |  |
| `media[].mediaType` | string |  |
| `media[].mimeType` | string |  |
| `media[].signedUrl` | string |  |
| `media[].size` | string |  |
| `media[].updatedAt` | string |  |
| `media[].uploadedBy` | string |  |
| `media[].visibility` | string |  |
| `media[].workspaceId` | string |  |
| `nextPageToken` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `GET /v1/media` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-media-files.md) for the provider-specific parameters and requirements.

