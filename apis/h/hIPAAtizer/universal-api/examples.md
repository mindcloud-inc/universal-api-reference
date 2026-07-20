# HIPAAtizer Universal API Examples

These examples use the MindCloud API key and HIPAAtizer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List All Locations

Retrieves all account locations from HIPAAtizer.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/list-all-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/list-all-locations?${params}`, {
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
      "createdAt": "string",
      "defaultScheduleId": "string",
      "description": "string",
      "email": "ava@example.com",
      "id": "string",
      "isDefault": true,
      "lat": 1,
      "lng": 1,
      "name": "Ava Chen",
      "phone": "string",
      "timeZoneId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List All Locations action reference](actions/list-all-locations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hIPAAtizer/latest/actions/list-all-locations).
