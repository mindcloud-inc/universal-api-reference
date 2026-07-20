# USGS Earthquake Hazards Universal API Examples

These examples use the MindCloud API key and USGS Earthquake Hazards connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Earthquakes

Finds earthquakes in USGS Earthquake Hazards by search parameters.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/search-earthquakes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/search-earthquakes?${params}`, {
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
      "bbox": [
        1
      ],
      "features": [
        {
          "geometry": {
            "coordinates": [
              1
            ],
            "type": "string"
          },
          "id": "string",
          "properties": {
            "detail": "string",
            "mag": 1,
            "place": "string",
            "status": "string",
            "time": 1,
            "title": "string",
            "updated": 1,
            "url": "https://example.com"
          }
        }
      ],
      "metadata": {
        "count": 1,
        "generated": 1,
        "status": 1,
        "title": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Earthquakes action reference](actions/search-earthquakes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uSGSEarthquakeHazards/latest/actions/search-earthquakes).
