# IPLocate Universal API Examples

These examples use the MindCloud API key and IPLocate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Lookup Current IP



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/lookup-current-ip?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/lookup-current-ip?${params}`, {
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
      "abuse": {},
      "asn": {},
      "calling_code": "string",
      "city": "string",
      "company": {},
      "continent": "string",
      "country": "string",
      "country_code": "string",
      "currency_code": "string",
      "hosting": {},
      "ip": "string",
      "is_anycast": true,
      "is_eu": true,
      "is_satellite": true,
      "latitude": 1,
      "longitude": 1,
      "postal_code": "string",
      "privacy": {},
      "subdivision": "string",
      "time_zone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Lookup Current IP action reference](actions/lookup-current-ip.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iPLocate/latest/actions/lookup-current-ip).
