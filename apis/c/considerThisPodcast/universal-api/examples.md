# Consider This Podcast Universal API Examples

These examples use the MindCloud API key and Consider This Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Episodes

Retrieves podcast episodes from Consider This Podcast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/considerThisPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/considerThisPodcast/latest/actions/list-episodes?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Episodes action reference](actions/list-episodes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/considerThisPodcast/latest/actions/list-episodes).
