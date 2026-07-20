# Mapulus: Create Location

Creates a new location in Mapulus.

```
POST https://connect.mindcloud.co/v1/universal/mapulus/latest/actions/create-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mapulus `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `layerId` | string | yes | The layer that will contain the location. |
| `lat` | number | no | Latitude in decimal degrees. |
| `lon` | number | no | Longitude in decimal degrees. |
| `label` | string | no | Short label for the location. |
| `title` | string | no | Display title for the location. |
| `address` | string | no | Address for the location. |
| `externalId` | string | no | External identifier for the location. |
| `travelContour` | boolean | no | Whether to generate a travel contour. |
| `contourMode` | string | no | Routing mode for contour generation. |
| `contourMetric` | string | no | Metric for contour generation. |
| `contourStyle` | string | no | Style for contour output. |
| `contourMinutes` | string | no | Travel time for contour generation in minutes. |
| `createOrUpdateCustomAttributes` | boolean | no | Whether to create or update custom attributes automatically. |
| `customAttributes[]` | array<object> | no | Custom attributes to attach to the location. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | The formatted address. |
| `contourMetric` | string | The contour metric. |
| `contourMinutes` | string | The contour duration value. |
| `contourMode` | string | The contour travel mode. |
| `contourStyle` | string | The contour style. |
| `createdAt` | date | When the location was created. |
| `customAttributes` | array<object> | Custom attributes attached to the location. |
| `externalId` | string | The provider-side external identifier. |
| `geocodingError` | boolean | Whether geocoding failed for the location. |
| `geocodingErrorType` | string | The geocoding error type, when present. |
| `id` | string | The location identifier. |
| `label` | string | The short label for the location. |
| `lat` | number | The latitude of the location. |
| `layerId` | string | The parent layer identifier. |
| `lon` | number | The longitude of the location. |
| `mapId` | string | The parent map identifier. |
| `object` | string | The resource type returned by Mapulus. |
| `title` | string | The title of the location. |
| `travelContour` | boolean | Whether a travel contour is enabled. |
| `updatedAt` | date | When the location was last updated. |

## Native endpoint

Through the native Mapulus API, this operation is `POST /api/v1/locations` (base URL `https://api.mapulus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-location.md) for the provider-specific parameters and requirements.

