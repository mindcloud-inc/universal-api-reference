# Xkcd Universal API Examples

These examples use the MindCloud API key and Xkcd connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Atom Feed

Retrieves the Atom comic feed from Xkcd.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-atom-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-atom-feed?${params}`, {
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
      "entry": [
        {}
      ],
      "id": "string",
      "link": "https://example.com",
      "summary": "string",
      "title": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Atom Feed action reference](actions/get-atom-feed.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xkcd/latest/actions/get-atom-feed).
