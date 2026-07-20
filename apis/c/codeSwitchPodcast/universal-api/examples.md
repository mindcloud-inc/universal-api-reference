# Code Switch Podcast Universal API Examples

These examples use the MindCloud API key and Code Switch Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Podcast Feed

Retrieves the Code Switch podcast RSS feed from NPR.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeSwitchPodcast/latest/actions/get-podcast-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeSwitchPodcast/latest/actions/get-podcast-feed?${params}`, {
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
      "data": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get Podcast Feed action reference](actions/get-podcast-feed.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/codeSwitchPodcast/latest/actions/get-podcast-feed).
