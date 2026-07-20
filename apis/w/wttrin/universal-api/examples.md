# wttr.in Universal API Examples

These examples use the MindCloud API key and wttr.in connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Weather Forecast JSON

Retrieves full weather forecast JSON from wttr.in.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wttrin/latest/actions/get-weather-forecast-json?connectionId=$CONNECTION_ID&location=London" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "London"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wttrin/latest/actions/get-weather-forecast-json?${params}`, {
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
      "current_condition": [
        {}
      ],
      "nearest_area": [
        {}
      ],
      "request": [
        {}
      ],
      "weather": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Weather Forecast JSON action reference](actions/get-weather-forecast-json.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wttrin/latest/actions/get-weather-forecast-json).
