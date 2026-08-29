# AXL Universal API Examples

These examples use the MindCloud API key and AXL connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Courses



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-courses?connectionId=$CONNECTION_ID&limit=25&offset=0&fields=%7Bid%2Cname%2CisPublished%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "fields": "{id,name,isPublished}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-courses?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Courses action reference](actions/get-courses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aXL/latest/actions/get-courses).
