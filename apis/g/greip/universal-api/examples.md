# Greip - Fraud Prevention Universal API Examples

These examples use the MindCloud API key and Greip - Fraud Prevention connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get IP Geolocation

Retrieves IP geolocation data from Greip.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-ip-geolocation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-ip-geolocation?${params}`, {
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
      "asn": {},
      "bogon": true,
      "cityName": "Ava Chen",
      "continentCode": "string",
      "continentGeoNameID": 1,
      "continentName": "Ava Chen",
      "countryCode": "string",
      "countryGeoNameID": 1,
      "countryName": "Ava Chen",
      "ip": "string",
      "iPNumber": 1,
      "ipType": "string",
      "latitude": "string",
      "longitude": "string",
      "regionName": "Ava Chen",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get IP Geolocation action reference](actions/get-ip-geolocation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/greip/latest/actions/get-ip-geolocation).
