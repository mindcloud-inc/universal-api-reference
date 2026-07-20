# Precisely Universal API Examples

These examples use the MindCloud API key and Precisely connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Typeahead Locations

Finds address suggestions in Precisely by partial location input.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/typeahead-locations?connectionId=$CONNECTION_ID&searchText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/precisely/latest/actions/typeahead-locations?${params}`, {
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
      "address": {
        "addressLastLine": "string",
        "addressNumber": "string",
        "areaName1": "Ava Chen",
        "areaName3": "Ava Chen",
        "country": "string",
        "formattedAddress": "string",
        "mainAddressLine": "string",
        "placeName": "Ava Chen",
        "postCode": "string",
        "streetName": "Ava Chen"
      },
      "geometry": {
        "coordinates": [
          1
        ],
        "type": "string"
      },
      "ranges": [
        {}
      ],
      "totalUnitCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Typeahead Locations action reference](actions/typeahead-locations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/precisely/latest/actions/typeahead-locations).
