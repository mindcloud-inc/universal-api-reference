# Twitch: List Streams

Retrieves live stream records from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-streams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-streams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-streams?${params}`, {
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
| `userId` | string | no | A user ID used to filter the list of streams. Specify this parameter up to 100 times. Accepts multiple values as an array. |
| `userLogin` | string | no | A user login name used to filter the list of streams. Specify this parameter up to 100 times. Accepts multiple values as an array. |
| `gameId` | string | no | A game ID used to filter the list of streams. Specify this parameter up to 100 times. Accepts multiple values as an array. |
| `type` | list | no | A stream type used to filter the list of streams. One of: `all`, `live`. |
| `language` | string | no | A language used to filter the list of streams. |
| `first` | number | no | The maximum number of objects to return. Maximum: 100. Default: 20. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | string | no | The cursor used to get the next page of results. |
| `before` | string | no | The cursor used to get the previous page of results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gameId": "string",
      "gameName": "Ava Chen",
      "id": "string",
      "isMature": true,
      "language": "string",
      "startedAt": "string",
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gameId` | string |  |
| `gameName` | string |  |
| `id` | string |  |
| `isMature` | boolean |  |
| `language` | string |  |
| `startedAt` | string |  |
| `tags[]` | string |  |
| `thumbnailUrl` | string |  |
| `title` | string |  |
| `type` | string |  |
| `userId` | string |  |
| `userLogin` | string |  |
| `userName` | string |  |
| `viewerCount` | number |  |

## Native endpoint

Through the native Twitch API, this operation is `GET /streams` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-streams.md) for the provider-specific parameters and requirements.

