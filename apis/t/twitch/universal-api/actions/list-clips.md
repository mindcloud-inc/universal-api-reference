# Twitch: List Clips

Retrieves clip records and metadata from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-clips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-clips?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-clips?${params}`, {
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
| `broadcasterId` | string | no | An ID that identifies the broadcaster whose video clips you want to get. |
| `gameId` | string | no | An ID that identifies the game whose clips you want to get. |
| `id` | string | no | An ID that identifies the clip to get. Include this parameter for each clip you want to fetch. Accepts multiple values as an array. |
| `startedAt` | date | no | The start date used to filter clips. Specify the date and time in RFC3339 format. |
| `endedAt` | date | no | The end date used to filter clips. If omitted, Twitch uses one week after the start date. |
| `first` | number | no | The maximum number of clips to return per page. Minimum 1, maximum 100. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | string | no | The cursor used to get the next page of results. |
| `before` | string | no | The cursor used to get the previous page of results. |
| `isFeatured` | boolean | no | Whether to return only featured clips. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "broadcasterId": "string",
      "broadcasterName": "Ava Chen",
      "createdAt": "string",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "duration": 1,
      "embedUrl": "https://example.com",
      "gameId": "string",
      "id": "string",
      "isFeatured": true,
      "language": "string",
      "thumbnailUrl": "https://example.com",
      "title": "string",
      "url": "https://example.com",
      "videoId": "string",
      "viewCount": 1,
      "vodOffset": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcasterId` | string |  |
| `broadcasterName` | string |  |
| `createdAt` | string |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `duration` | number |  |
| `embedUrl` | string |  |
| `gameId` | string |  |
| `id` | string |  |
| `isFeatured` | boolean |  |
| `language` | string |  |
| `thumbnailUrl` | string |  |
| `title` | string |  |
| `url` | string |  |
| `videoId` | string |  |
| `viewCount` | number |  |
| `vodOffset` | object |  |

## Native endpoint

Through the native Twitch API, this operation is `GET /clips` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clips.md) for the provider-specific parameters and requirements.

