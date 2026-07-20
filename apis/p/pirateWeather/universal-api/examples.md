# Pirate Weather Universal API Examples

These examples use the MindCloud API key and Pirate Weather connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Forecast

Retrieves a weather forecast from Pirate Weather.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pirateWeather/latest/actions/get-forecast?connectionId=$CONNECTION_ID&latitude=1&longitude=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1",
  "longitude": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pirateWeather/latest/actions/get-forecast?${params}`, {
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
      "alerts": [
        {}
      ],
      "currently": {},
      "daily": {},
      "elevation": 1,
      "flags": {},
      "hourly": {},
      "latitude": 1,
      "longitude": 1,
      "minutely": {},
      "offset": 1,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Forecast action reference](actions/get-forecast.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pirateWeather/latest/actions/get-forecast).
