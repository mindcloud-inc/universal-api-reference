# Twitch: Search Channels

Searches Twitch channels using a query.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/search-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/search-channels?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/search-channels?${params}`, {
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
| `query` | string | yes | The URI-encoded search string. This may contain a maximum of 100 characters. |
| `liveOnly` | boolean | no | A Boolean value that determines whether the response includes only channels that are currently streaming live. |
| `first` | number | no | The maximum number of objects to return. Maximum: 100. Default: 20. |

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
      "broadcasterLanguage": "string",
      "broadcasterLogin": "string",
      "displayName": "Ava Chen",
      "gameId": "string",
      "gameName": "Ava Chen",
      "id": "string",
      "isLive": true,
      "startedAt": "string",
      "tags": [
        "string"
      ],
      "thumbnailUrl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcasterLanguage` | string |  |
| `broadcasterLogin` | string |  |
| `displayName` | string |  |
| `gameId` | string |  |
| `gameName` | string |  |
| `id` | string |  |
| `isLive` | boolean |  |
| `startedAt` | string |  |
| `tags[]` | string |  |
| `thumbnailUrl` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Twitch API, this operation is `GET /search/channels` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-channels.md) for the provider-specific parameters and requirements.

