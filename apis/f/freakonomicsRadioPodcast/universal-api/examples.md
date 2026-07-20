# Freakonomics Radio Podcast Universal API Examples

These examples use the MindCloud API key and Freakonomics Radio Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Episodes

Retrieves episodes from the Freakonomics Radio RSS feed.

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

Example response:

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

See the full [List Episodes action reference](actions/list-episodes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freakonomicsRadioPodcast/latest/actions/list-episodes).
