# TimeAPI Universal API Examples

These examples use the MindCloud API key and TimeAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current UTC Time

Retrieves the current UTC time from TimeAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-utc-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-utc-time?${params}`, {
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
      "utc_time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Current UTC Time action reference](actions/get-current-utc-time.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timeAPI/latest/actions/get-current-utc-time).
