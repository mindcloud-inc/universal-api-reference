# Zillow Zestimates Universal API Examples

These examples use the MindCloud API key and Zillow Zestimates connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List zestimates

Retrieves current property, rental, and foreclosure Zestimates from Zillow.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowZestimates/latest/actions/list-zestimates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowZestimates/latest/actions/list-zestimates?${params}`, {
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
      "BridgeModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "city": "string",
      "highPercent": 1,
      "houseNumber": "string",
      "id": "string",
      "Latitude": 1,
      "Longitude": 1,
      "lowPercent": 1,
      "postalCode": "string",
      "rentalHighPercent": 1,
      "rentalLowPercent": 1,
      "rentalTimestamp": "2026-05-07T12:00:00.000Z",
      "rentalZestimate": 1,
      "state": "string",
      "streetName": "Ava Chen",
      "streetSuffix": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "unitNumber": "string",
      "zestimate": 1,
      "zillowUrl": "https://example.com",
      "zpid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List zestimates action reference](actions/list-zestimates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zillowZestimates/latest/actions/list-zestimates).
