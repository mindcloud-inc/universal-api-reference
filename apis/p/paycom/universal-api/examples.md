# Paycom Universal API Examples

These examples use the MindCloud API key and Paycom connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Locations



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycom/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycom/latest/actions/list-locations?${params}`, {
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
      "address": "string",
      "city": "string",
      "country": "string",
      "description": "string",
      "eEOCUnitNumber": "string",
      "facilityId": "string",
      "hiringSite": true,
      "locationHidden": true,
      "locationid": 1,
      "state": "string",
      "vETS4212HiringLocation": true,
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Locations action reference](actions/list-locations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paycom/latest/actions/list-locations).
