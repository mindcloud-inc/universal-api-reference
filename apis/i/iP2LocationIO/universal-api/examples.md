# IP2Location IO Universal API Examples

These examples use the MindCloud API key and IP2Location IO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get IP Geolocation



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2LocationIO/latest/actions/get-ip-geolocation?connectionId=$CONNECTION_ID&ip=8.8.8.8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "8.8.8.8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iP2LocationIO/latest/actions/get-ip-geolocation?${params}`, {
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
      "as": "string",
      "asn": "string",
      "city_name": "Ava Chen",
      "country_code": "string",
      "country_name": "Ava Chen",
      "ip": "string",
      "is_proxy": true,
      "latitude": 1,
      "longitude": 1,
      "region_name": "Ava Chen",
      "time_zone": "string",
      "zip_code": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get IP Geolocation action reference](actions/get-ip-geolocation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iP2LocationIO/latest/actions/get-ip-geolocation).
