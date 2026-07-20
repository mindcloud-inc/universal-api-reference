# Finnish Railway Traffic Universal API Examples

These examples use the MindCloud API key and Finnish Railway Traffic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get latest train by number

Retrieves the latest train by number from Finnish Railway Traffic.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/get-latest-train-by-number?connectionId=$CONNECTION_ID&trainNumber=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trainNumber": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/get-latest-train-by-number?${params}`, {
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
      "cancelled": true,
      "commuterLineID": "string",
      "departureDate": "2026-05-07T12:00:00.000Z",
      "runningCurrently": true,
      "timeTableRows": [
        {}
      ],
      "trainCategory": "string",
      "trainNumber": 1,
      "trainType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get latest train by number action reference](actions/get-latest-train-by-number.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/finnishRailwayTraffic/latest/actions/get-latest-train-by-number).
