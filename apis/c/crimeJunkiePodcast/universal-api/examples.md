# Crime Junkie Podcast Universal API Examples

These examples use the MindCloud API key and Crime Junkie Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Recent Episodes

Retrieves recent podcast episodes from Crime Junkie Podcast.

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

Example response:

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

See the full [List Recent Episodes action reference](actions/list-recent-episodes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crimeJunkiePodcast/latest/actions/list-recent-episodes).
