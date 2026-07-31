# Where the ISS at Universal API Examples

These examples use the MindCloud API key and Where the ISS at connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Coordinate Timezone



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/get-coordinate-timezone?connectionId=$CONNECTION_ID&latitude=1&longitude=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1",
  "longitude": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/get-coordinate-timezone?${params}`, {
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
      "country_code": "string",
      "latitude": "string",
      "longitude": "string",
      "map_url": "https://example.com",
      "offset": 1,
      "timezone_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Coordinate Timezone action reference](actions/get-coordinate-timezone.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whereTheISSAt/latest/actions/get-coordinate-timezone).
