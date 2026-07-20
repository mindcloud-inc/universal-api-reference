# Bokun Universal API Examples

These examples use the MindCloud API key and Bokun connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Time Zones

Retrieves supported time zones from Bokun.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-time-zones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-time-zones?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Time Zones action reference](actions/list-time-zones.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bokun/latest/actions/list-time-zones).
