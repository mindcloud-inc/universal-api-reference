# Fresh Air Podcast Universal API Examples

These examples use the MindCloud API key and Fresh Air Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Episodes



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshAirPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshAirPodcast/latest/actions/list-episodes?${params}`, {
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
      "content:encoded": {},
      "description": {},
      "enclosure": {},
      "guid": "string",
      "itunes:block": "string",
      "itunes:duration": "string",
      "itunes:episodeType": "string",
      "itunes:explicit": "string",
      "itunes:image": {},
      "itunes:title": "string",
      "link": "https://example.com",
      "media:thumbnail": {},
      "pubDate": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Episodes action reference](actions/list-episodes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freshAirPodcast/latest/actions/list-episodes).
