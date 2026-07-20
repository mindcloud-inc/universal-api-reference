# Crime Junkie Podcast: List Recent Episodes

Retrieves recent podcast episodes from Crime Junkie Podcast.

```
GET https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-recent-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crime Junkie Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-recent-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-recent-episodes?${params}`, {
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
      "author": "string",
      "categories": [
        "string"
      ],
      "description": "string",
      "guid": "string",
      "link": "https://example.com",
      "pubDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string | Episode post author exposed by the RSS item. |
| `categories` | array<string> | Episode categories exposed in the RSS item. |
| `description` | string | Episode summary or excerpt from the RSS item. |
| `guid` | string | Episode GUID from the RSS feed item. |
| `link` | string | Canonical episode URL on the official Crime Junkie site. |
| `pubDate` | date | Episode publication date from the RSS feed. |
| `title` | string | Episode title from the Crime Junkie RSS item. |

## Native endpoint

Through the native Crime Junkie Podcast API, this operation is `GET /feed/` (base URL `https://crimejunkiepodcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-episodes.md) for the provider-specific parameters and requirements.

