# Pinterest: List Boards

Retrieves the current user's boards from Pinterest.

```
GET https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-boards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinterest `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-boards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-boards?${params}`, {
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
      "boardPinsModifiedAt": "2026-05-07T12:00:00.000Z",
      "collaboratorCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "followerCount": 1,
      "id": "string",
      "media": {
        "imageCoverUrl": "https://example.com",
        "pinThumbnailUrls": [
          "https://example.com"
        ]
      },
      "name": "Ava Chen",
      "owner": {
        "username": "Ava Chen"
      },
      "pinCount": 1,
      "privacy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boardPinsModifiedAt` | date |  |
| `collaboratorCount` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `followerCount` | number |  |
| `id` | string |  |
| `media.imageCoverUrl` | string |  |
| `media.pinThumbnailUrls[]` | string |  |
| `name` | string |  |
| `owner.username` | string |  |
| `pinCount` | number |  |
| `privacy` | string |  |

## Native endpoint

Through the native Pinterest API, this operation is `GET boards` (base URL `https://api.pinterest.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-boards.md) for the provider-specific parameters and requirements.

