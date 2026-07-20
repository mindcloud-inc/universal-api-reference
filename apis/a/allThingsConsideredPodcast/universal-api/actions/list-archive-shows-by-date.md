# All Things Considered Podcast: List Archive Shows By Date

Retrieves archived shows by date from All Things Considered Podcast.

```
GET https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/list-archive-shows-by-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a All Things Considered Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/list-archive-shows-by-date?connectionId=$CONNECTION_ID&date=2026-04-29" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2026-04-29"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/list-archive-shows-by-date?${params}`, {
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
| `date` | string | yes | Archive date to load, formatted as YYYY-MM-DD. Default: `2026-04-29`. Example: `2026-04-29`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliation": "string",
      "audioUrl": "https://example.com",
      "available": true,
      "duration": 1,
      "mediaId": "string",
      "program": "string",
      "slug": "string",
      "storyId": "string",
      "storyUrl": "https://example.com",
      "title": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliation` | string |  |
| `audioUrl` | string |  |
| `available` | boolean |  |
| `duration` | number |  |
| `mediaId` | string |  |
| `program` | string |  |
| `slug` | string |  |
| `storyId` | string |  |
| `storyUrl` | string |  |
| `title` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native All Things Considered Podcast API, this operation is `GET /programs/all-things-considered/archive` (base URL `https://www.npr.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-archive-shows-by-date.md) for the provider-specific parameters and requirements.

