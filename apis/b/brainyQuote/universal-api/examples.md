# BrainyQuote Universal API Examples

These examples use the MindCloud API key and BrainyQuote connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Art Quote of the Day

Retrieves the BrainyQuote art quote of the day feed.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brainyQuote/latest/actions/get-art-quote-of-the-day?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brainyQuote/latest/actions/get-art-quote-of-the-day?${params}`, {
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
      "description": "string",
      "guid": "https://example.com",
      "link": "https://example.com",
      "pubDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Art Quote of the Day action reference](actions/get-art-quote-of-the-day.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/brainyQuote/latest/actions/get-art-quote-of-the-day).
