# Cloudmersive Universal API Examples

These examples use the MindCloud API key and Cloudmersive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Date and Time

Retrieves the current date and time from Cloudmersive.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-current-date-and-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-current-date-and-time?${params}`, {
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
      "now": "2026-05-07T12:00:00.000Z",
      "nowGmt": "2026-05-07T12:00:00.000Z",
      "successful": true
    }
  ],
  "meta": {}
}
```

See the full [Get Current Date and Time action reference](actions/get-current-date-and-time.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudmersive/latest/actions/get-current-date-and-time).
