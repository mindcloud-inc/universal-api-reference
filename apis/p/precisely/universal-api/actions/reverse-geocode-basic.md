# Precisely: Reverse Geocode (Basic)

Retrieves address details from Precisely for a coordinate.

```
GET https://connect.mindcloud.co/v1/universal/precisely/latest/actions/reverse-geocode-basic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Precisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/reverse-geocode-basic?connectionId=$CONNECTION_ID&x=1&y=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "x": "1",
  "y": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/precisely/latest/actions/reverse-geocode-basic?${params}`, {
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
| `x` | number | yes | Longitude in degrees, for example: -79.391165. |
| `y` | number | yes | Latitude in degrees, for example: 43.643469. |
| `country` | string | no | ISO country code or country name. |
| `coordSysName` | string | no | Coordinate system to convert the geometry to, in codespace:code format, for example EPSG:4326. |
| `distance` | number | no | Search radius around the input coordinates. |
| `distanceUnits` | string | no | Unit of measurement for the search distance. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "areaName1": "Ava Chen",
        "areaName2": "Ava Chen",
        "areaName3": "Ava Chen",
        "areaName4": "Ava Chen",
        "country": "string",
        "customFields": {
          "GENERIC_FIELD_1": "string",
          "REVERSE_GEOCODE_DISTANCE": "string",
          "REVERSE_GEOCODE_DISTANCE_UNIT": "string"
        }
      },
      "geometry": {
        "coordinates": [
          1
        ],
        "type": "string"
      },
      "precisionCode": "string",
      "precisionLevel": 1,
      "ranges": [
        {}
      ],
      "sourceDictionary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.areaName1` | string | Top-level administrative area, typically state or province. |
| `address.areaName2` | string | Secondary administrative area, typically county or district. |
| `address.areaName3` | string | City or locality name. |
| `address.areaName4` | string | Sub-city locality or neighborhood name. |
| `address.country` | string | Country code or country name. |
| `address.customFields.GENERIC_FIELD_1` | string | Provider-specific location identifier returned by Precisely. |
| `address.customFields.REVERSE_GEOCODE_DISTANCE` | string | Distance from the input point to the matched location. |
| `address.customFields.REVERSE_GEOCODE_DISTANCE_UNIT` | string | Unit used for the reverse-geocode distance. |
| `geometry.coordinates` | array<number> | Longitude and latitude coordinates. |
| `geometry.type` | string | GeoJSON geometry type. |
| `precisionCode` | string | Precisely precision code for the reverse geocode match. |
| `precisionLevel` | number | Matched precision level returned for the candidate. |
| `ranges` | array<object> | Range metadata returned for the candidate. |
| `sourceDictionary` | string | Precisely source dictionary identifier. |

## Native endpoint

Through the native Precisely API, this operation is `GET /geocode/v1/basic/reverseGeocode` (base URL `https://api.precisely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-geocode-basic.md) for the provider-specific parameters and requirements.

