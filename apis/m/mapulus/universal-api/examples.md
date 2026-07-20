# Mapulus Universal API Examples

These examples use the MindCloud API key and Mapulus connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Maps

Retrieves all maps from your Mapulus account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mapulus/latest/actions/list-maps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mapulus/latest/actions/list-maps?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "object": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Maps action reference](actions/list-maps.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mapulus/latest/actions/list-maps).

## Create Location

Creates a new location in Mapulus.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mapulus/latest/actions/create-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "layerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mapulus/latest/actions/create-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "layerId": "string"
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
      "address": "string",
      "contourMetric": "string",
      "contourMinutes": "string",
      "contourMode": "string",
      "contourStyle": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customAttributes": [
        {}
      ],
      "externalId": "string",
      "geocodingError": true,
      "geocodingErrorType": "string",
      "id": "string",
      "label": "string",
      "lat": 1,
      "layerId": "string",
      "lon": 1,
      "mapId": "string",
      "object": "string",
      "title": "string",
      "travelContour": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Location action reference](actions/create-location.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mapulus/latest/actions/create-location).
