# USGS Earthquake Hazards: Get Regions For Coordinates

Retrieves regions for latitude and longitude coordinates.

```
GET https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/get-regions-for-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USGS Earthquake Hazards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/get-regions-for-coordinates?connectionId=$CONNECTION_ID&latitude=39.5&longitude=-105" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "39.5",
  "longitude": "-105"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/get-regions-for-coordinates?${params}`, {
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
| `latitude` | number | yes | Latitude in decimal degrees of the point to look up. Example: `39.5`. |
| `longitude` | number | yes | Longitude in decimal degrees of the point to look up. Example: `-105`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeGeometry` | boolean | no | Set true to include polygon points for selected regions. Default: `false`. |
| `type` | string | no | Comma-separated Geoserve region types to return. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. Default: `admin,fe,tectonic`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin": {
        "features": [
          {
            "properties": {
              "country": "string",
              "iso": "string",
              "region": "string"
            }
          }
        ]
      },
      "fe": {
        "features": [
          {
            "properties": {
              "name": "Ava Chen"
            }
          }
        ]
      },
      "tectonic": {
        "features": [
          {
            "properties": {
              "name": "Ava Chen",
              "summary": "string"
            }
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | object | Administrative region FeatureCollection. |
| `admin.features` | array<object> | Administrative region features. |
| `admin.features[].properties.country` | string | Country name. |
| `admin.features[].properties.iso` | string | Country code. |
| `admin.features[].properties.region` | string | Region name. |
| `fe` | object | FE region FeatureCollection. |
| `fe.features[].properties.name` | string | FE region name. |
| `tectonic` | object | Tectonic region FeatureCollection. |
| `tectonic.features[].properties.name` | string | Tectonic region name. |
| `tectonic.features[].properties.summary` | string | Tectonic summary content. |

## Native endpoint

Through the native USGS Earthquake Hazards API, this operation is `GET /ws/geoserve/regions.json` (base URL `https://earthquake.usgs.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-regions-for-coordinates.md) for the provider-specific parameters and requirements.

