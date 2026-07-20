# Placekey Universal API Examples

These examples use the MindCloud API key and Placekey connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Placekey

Retrieves a Placekey for one location in Placekey.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placekey/latest/actions/get-placekey?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placekey/latest/actions/get-placekey?${params}`, {
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
      "addressPlacekey": "string",
      "buildingPlacekey": "string",
      "confidenceScore": 1,
      "geocode": {},
      "normalizedAddress": "string",
      "placekey": "string",
      "queryId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Placekey action reference](actions/get-placekey.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/placekey/latest/actions/get-placekey).
