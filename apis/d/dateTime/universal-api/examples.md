# Date & Time Universal API Examples

These examples use the MindCloud API key and Date & Time connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Date & Time Service Counts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/get-date-time-service-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/get-date-time-service-counts?${params}`, {
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
      "channel": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Date & Time Service Counts action reference](actions/get-date-time-service-counts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dateTime/latest/actions/get-date-time-service-counts).
