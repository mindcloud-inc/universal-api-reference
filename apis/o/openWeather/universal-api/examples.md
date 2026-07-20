# OpenWeather Universal API Examples

These examples use the MindCloud API key and OpenWeather connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Weather

Retrieves current weather from OpenWeather by coordinates.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-current-weather?connectionId=$CONNECTION_ID&lat=1&lon=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "1",
  "lon": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-current-weather?${params}`, {
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
      "base": "string",
      "clouds": {},
      "cod": 1,
      "coord": {},
      "dt": 1,
      "id": 1,
      "main": {},
      "name": "Ava Chen",
      "sys": {},
      "timezone": 1,
      "visibility": 1,
      "weather": [
        {}
      ],
      "wind": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Current Weather action reference](actions/get-current-weather.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openWeather/latest/actions/get-current-weather).

## Create Solar Location

Creates a solar location in OpenWeather.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/create-solar-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "coordinates": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/create-solar-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "coordinates": {}
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "coordinates": {},
      "location_id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Solar Location action reference](actions/create-solar-location.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openWeather/latest/actions/create-solar-location).
