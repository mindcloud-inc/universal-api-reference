# Mapulus: List Locations

Retrieves locations from your Mapulus account.

```
GET https://connect.mindcloud.co/v1/universal/mapulus/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mapulus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mapulus/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mapulus/latest/actions/list-locations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mapId` | string | no | Filter locations by map ID. |
| `layerId` | string | no | Filter locations by layer ID. |
| `externalId` | string | no | Filter locations by external ID. |
| `nearest.lat` | number | no | Latitude for nearest-location search. |
| `nearest.lon` | number | no | Longitude for nearest-location search. |
| `nearest.address` | string | no | Address for nearest-location search. |
| `nearest.sortBy` | string | no | Sort nearest results by distance or time. |
| `nearest.profile` | string | no | Routing profile for nearest-location search. |
| `nearest.liveTraffic` | string | no | Whether to include live traffic in nearest-location search. |
| `nearest.limit` | number | no | Limit nearest-location results. |

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
      "description": "string",
      "email": "ava@example.com",
      "externalId": "string",
      "focusForProfileId": "string",
      "geocodingError": true,
      "geocodingErrorType": "string",
      "id": "string",
      "label": "string",
      "lat": 1,
      "layerId": "string",
      "lon": 1,
      "mapId": "string",
      "object": "string",
      "phoneNumber": "string",
      "primaryImage": "string",
      "rating": 1,
      "ratingCount": 1,
      "ratingSource": "string",
      "title": "string",
      "travelContour": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "website": "string"
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
| `description` | string | The freeform description for the location. |
| `email` | string | The email address for the location. |
| `externalId` | string | The provider-side external identifier. |
| `focusForProfileId` | string | The routing profile focus identifier, when present. |
| `geocodingError` | boolean | Whether geocoding failed for the location. |
| `geocodingErrorType` | string | The geocoding error type, when present. |
| `id` | string | The location identifier. |
| `label` | string | The short label for the location. |
| `lat` | number | The latitude of the location. |
| `layerId` | string | The parent layer identifier. |
| `lon` | number | The longitude of the location. |
| `mapId` | string | The parent map identifier. |
| `object` | string | The resource type returned by Mapulus. |
| `phoneNumber` | string | The phone number for the location. |
| `primaryImage` | string | The primary image URL for the location. |
| `rating` | number | The location rating, when present. |
| `ratingCount` | number | The number of ratings, when present. |
| `ratingSource` | string | The rating source, when present. |
| `title` | string | The title of the location. |
| `travelContour` | boolean | Whether a travel contour is enabled. |
| `updatedAt` | date | When the location was last updated. |
| `website` | string | The website URL for the location. |

## Native endpoint

Through the native Mapulus API, this operation is `GET /api/v1/locations` (base URL `https://api.mapulus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

