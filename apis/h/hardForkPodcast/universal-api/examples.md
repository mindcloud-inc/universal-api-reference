# Hard Fork Podcast Universal API Examples

These examples use the MindCloud API key and Hard Fork Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Episodes

Retrieves podcast episodes from Hard Fork Podcast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hardForkPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hardForkPodcast/latest/actions/list-episodes?${params}`, {
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
      "content:encoded": {},
      "description": {},
      "enclosure": {},
      "guid": "string",
      "itunes:duration": "string",
      "itunes:episode": "string",
      "itunes:episodeType": "string",
      "itunes:explicit": "string",
      "itunes:subtitle": "string",
      "itunes:summary": "string",
      "link": "https://example.com",
      "pubDate": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Episodes action reference](actions/list-episodes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hardForkPodcast/latest/actions/list-episodes).
