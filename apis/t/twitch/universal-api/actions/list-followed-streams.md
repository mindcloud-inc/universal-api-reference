# Twitch: List Followed Streams

Retrieves followed live streams from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-followed-streams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-followed-streams?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-followed-streams?${params}`, {
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
| `userId` | string | yes | The ID of the user whose followed live streams you want to get. |
| `first` | number | no | The maximum number of items to return per page. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | string | no | The cursor used to get the next page of results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "gameId": "string",
          "gameName": "Ava Chen",
          "id": "string",
          "isMature": true,
          "language": "string",
          "startedAt": "string",
          "tagIds": [
            "string"
          ],
          "tags": [
            "string"
          ],
          "thumbnailUrl": "https://example.com",
          "title": "string",
          "type": "string",
          "userId": "string",
          "userLogin": "string",
          "userName": "Ava Chen",
          "viewerCount": 1
        }
      ],
      "pagination": {
        "cursor": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Followed live stream rows. |
| `data[].gameId` | string | Game or category identifier. |
| `data[].gameName` | string | Game or category name. |
| `data[].id` | string | Stream identifier. |
| `data[].isMature` | boolean | Whether the stream is flagged as mature. |
| `data[].language` | string | Stream language code. |
| `data[].startedAt` | string | Timestamp when the stream started. |
| `data[].tagIds` | array<string> | Deprecated tag identifier list. |
| `data[].tags` | array<string> | Stream tags. |
| `data[].thumbnailUrl` | string | Preview thumbnail URL. |
| `data[].title` | string | Stream title. |
| `data[].type` | string | Stream type. |
| `data[].userId` | string | Broadcaster user identifier. |
| `data[].userLogin` | string | Broadcaster login name. |
| `data[].userName` | string | Broadcaster display name. |
| `data[].viewerCount` | number | Current viewer count. |
| `pagination` | object | Pagination cursor payload. |
| `pagination.cursor` | string | Cursor for the next page of results. |

## Native endpoint

Through the native Twitch API, this operation is `GET /streams/followed` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-followed-streams.md) for the provider-specific parameters and requirements.

