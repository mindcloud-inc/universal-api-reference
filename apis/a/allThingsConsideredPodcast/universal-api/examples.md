# All Things Considered Podcast Universal API Examples

These examples use the MindCloud API key and All Things Considered Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Stories

Retrieves recent stories from All Things Considered Podcast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/list-stories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/list-stories?${params}`, {
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
      "content:encoded": {
        "_cdata": "string"
      },
      "dc:creator": "string",
      "description": "string",
      "guid": "string",
      "link": "https://example.com",
      "pubDate": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Stories action reference](actions/list-stories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/allThingsConsideredPodcast/latest/actions/list-stories).
