# IP2Location.io IP Geolocation Universal API Examples

These examples use the MindCloud API key and IP2Location.io IP Geolocation connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get IP Geolocation

Retrieves IP geolocation details from IP2Location.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2LocationioIPGeolocationAPI/latest/actions/get-ip-geolocation?connectionId=$CONNECTION_ID&ip=8.8.8.8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "8.8.8.8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iP2LocationioIPGeolocationAPI/latest/actions/get-ip-geolocation?${params}`, {
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
      "cityName": "Ava Chen",
      "countryCode": "string",
      "countryName": "Ava Chen",
      "ip": "string",
      "isProxy": true,
      "latitude": 1,
      "longitude": 1,
      "regionName": "Ava Chen",
      "timeZone": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get IP Geolocation action reference](actions/get-ip-geolocation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iP2LocationioIPGeolocationAPI/latest/actions/get-ip-geolocation).
