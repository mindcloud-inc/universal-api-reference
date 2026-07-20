# Instapaper: List Bookmarks



```
GET https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/list-bookmarks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instapaper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/list-bookmarks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/list-bookmarks?${params}`, {
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
| `folderId` | string | no | Optional folder selector: unread, starred, archive, or a folder ID from List Folders. |
| `have` | string | no | Optional comma-separated bookmark state list used for sync and progress updates. |
| `highlights` | string | no | Optional dash-delimited list of highlight IDs the client already has. |
| `limit` | string | no | Optional number of bookmarks to return, between 1 and 500. Default is 25. |
| `tag` | string | no | Optional tag filter. Only used when folder_id is not provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookmarks": [
        {
          "bookmarkId": 1,
          "description": "string",
          "hash": "string",
          "progress": 1,
          "progressTimestamp": 1,
          "title": "string",
          "type": "string",
          "url": "https://example.com"
        }
      ],
      "deleteIds": [
        1
      ],
      "highlights": [
        {
          "bookmarkId": 1,
          "highlightId": 1,
          "position": 1,
          "text": "string",
          "time": 1,
          "type": "string"
        }
      ],
      "user": {
        "type": "string",
        "userId": 1,
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookmarks[].bookmarkId` | number |  |
| `bookmarks[].description` | string |  |
| `bookmarks[].hash` | string |  |
| `bookmarks[].progress` | number |  |
| `bookmarks[].progressTimestamp` | number |  |
| `bookmarks[].title` | string |  |
| `bookmarks[].type` | string |  |
| `bookmarks[].url` | string |  |
| `deleteIds` | array<number> |  |
| `highlights[].bookmarkId` | number |  |
| `highlights[].highlightId` | number |  |
| `highlights[].position` | number |  |
| `highlights[].text` | string |  |
| `highlights[].time` | number |  |
| `highlights[].type` | string |  |
| `user.type` | string |  |
| `user.userId` | number |  |
| `user.username` | string |  |

## Native endpoint

Through the native Instapaper API, this operation is `POST /api/1/bookmarks/list` (base URL `https://www.instapaper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bookmarks.md) for the provider-specific parameters and requirements.

