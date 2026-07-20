# Freakonomics Radio Podcast: List Episodes

Retrieves episodes from the Freakonomics Radio RSS feed.

```
GET https://connect.mindcloud.co/v1/universal/freakonomicsRadioPodcast/latest/actions/list-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freakonomics Radio Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freakonomicsRadioPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freakonomicsRadioPodcast/latest/actions/list-episodes?${params}`, {
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
      "contentEncoded": "string",
      "description": "string",
      "enclosure": {},
      "guid": "string",
      "itunesAuthor": "string",
      "itunesDuration": "string",
      "itunesEpisode": 1,
      "itunesEpisodeType": "string",
      "itunesExplicit": true,
      "itunesSubtitle": "string",
      "itunesSummary": "string",
      "itunesTitle": "string",
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
| `author` | string | Episode author string from the RSS item. |
| `contentEncoded` | string | Full encoded episode content HTML when provided. |
| `description` | string | Episode description HTML from the RSS item. |
| `enclosure` | object | Audio enclosure metadata for the episode. |
| `guid` | string | RSS item GUID. |
| `itunesAuthor` | string | Apple Podcasts author string. |
| `itunesDuration` | string | Apple Podcasts duration string. |
| `itunesEpisode` | number | Apple Podcasts episode number when provided. |
| `itunesEpisodeType` | string | Apple Podcasts episode type. |
| `itunesExplicit` | boolean | Whether the episode is marked explicit. |
| `itunesSubtitle` | string | Apple Podcasts episode subtitle. |
| `itunesSummary` | string | Apple Podcasts episode summary. |
| `itunesTitle` | string | Apple Podcasts episode title. |
| `link` | string | Canonical episode or show link from the RSS item. |
| `pubDate` | date | Episode publish date from the RSS item. |
| `title` | string | Episode title. |

## Native endpoint

Through the native Freakonomics Radio Podcast API, this operation is `GET /Y8lFbOT4` (base URL `https://feeds.simplecast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episodes.md) for the provider-specific parameters and requirements.

