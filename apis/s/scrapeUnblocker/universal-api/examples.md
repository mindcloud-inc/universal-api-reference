# ScrapeUnblocker Universal API Examples

These examples use the MindCloud API key and ScrapeUnblocker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Page Source

Retrieves page source from ScrapeUnblocker.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeUnblocker/latest/actions/get-page-source?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeUnblocker/latest/actions/get-page-source?${params}`, {
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Page Source action reference](actions/get-page-source.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapeUnblocker/latest/actions/get-page-source).
