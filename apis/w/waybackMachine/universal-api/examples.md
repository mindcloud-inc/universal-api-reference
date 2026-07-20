# Wayback Machine Universal API Examples

These examples use the MindCloud API key and Wayback Machine connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check URL Availability

Retrieves archived snapshot availability for a URL in Wayback Machine.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/check-url-availability?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/check-url-availability?${params}`, {
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
      "archived_snapshots": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Check URL Availability action reference](actions/check-url-availability.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/waybackMachine/latest/actions/check-url-availability).
