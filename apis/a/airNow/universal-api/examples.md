# AirNow Universal API Examples

These examples use the MindCloud API key and AirNow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Current Observations by Zip Code

Retrieves current air quality observations from AirNow by zip code.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-current-observations-by-zip-code?connectionId=$CONNECTION_ID&zipCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zipCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-current-observations-by-zip-code?${params}`, {
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
      "aqi": 1,
      "category": {
        "name": "Ava Chen",
        "number": 1
      },
      "dateObserved": "2026-05-07T12:00:00.000Z",
      "hourObserved": 1,
      "latitude": 1,
      "localTimeZone": "string",
      "longitude": 1,
      "parameterName": "Ava Chen",
      "reportingArea": "string",
      "stateCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Current Observations by Zip Code action reference](actions/list-current-observations-by-zip-code.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airNow/latest/actions/list-current-observations-by-zip-code).
