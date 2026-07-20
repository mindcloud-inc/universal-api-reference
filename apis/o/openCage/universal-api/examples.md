# OpenCage Universal API Examples

These examples use the MindCloud API key and OpenCage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Forward Geocode

Finds location details in OpenCage by address or place name.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openCage/latest/actions/forward-geocode?connectionId=$CONNECTION_ID&q=Frauenplan%201%2C%2099423%20Weimar%2C%20Germany" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "Frauenplan 1, 99423 Weimar, Germany"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openCage/latest/actions/forward-geocode?${params}`, {
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
      "documentation": "https://example.com",
      "licenses": [
        {}
      ],
      "rate": {},
      "results": [
        {}
      ],
      "status": {},
      "thanks": "string",
      "timestamp": {},
      "total_results": 1
    }
  ],
  "meta": {}
}
```

See the full [Forward Geocode action reference](actions/forward-geocode.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openCage/latest/actions/forward-geocode).
