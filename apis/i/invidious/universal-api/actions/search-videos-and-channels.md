# Invidious: Search Videos And Channels



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/search-videos-and-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/search-videos-and-channels?connectionId=$CONNECTION_ID&query=ambient%20music" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "ambient music"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/search-videos-and-channels?${params}`, {
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
| `date` | string | no | Search date filter: hour, today, week, month, or year. |
| `duration` | string | no | Search duration filter: short, medium, or long. |
| `features` | string | no | Comma-separated search features such as hd, subtitles, 3d, live, or 4k. Accepts multiple values in one string, delimited by `,`. |
| `page` | number | no | Search result page number. Example: `1`. |
| `query` | string | yes | Search text. Example: `ambient music`. |
| `sort` | string | no | Search sort: relevance or views. |
| `type` | string | no | Search result type: video, playlist, channel, movie, show, or all. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `region` | string | no | ISO 3166 country code. Example: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "authorId": "string",
      "lengthSeconds": 1,
      "title": "string",
      "type": "string",
      "videoId": "string",
      "viewCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `authorId` | string |  |
| `lengthSeconds` | number |  |
| `title` | string |  |
| `type` | string |  |
| `videoId` | string |  |
| `viewCount` | number |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /search` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-videos-and-channels.md) for the provider-specific parameters and requirements.

