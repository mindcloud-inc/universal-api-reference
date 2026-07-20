# screenshot.fyi Universal API Examples

These examples use the MindCloud API key and screenshot.fyi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Take Screenshot



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenshotfyi/latest/actions/take-screenshot?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenshotfyi/latest/actions/take-screenshot?${params}`, {
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
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Take Screenshot action reference](actions/take-screenshot.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/screenshotfyi/latest/actions/take-screenshot).
