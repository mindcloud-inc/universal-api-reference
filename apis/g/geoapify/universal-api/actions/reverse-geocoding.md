# Geoapify Geocode: Reverse Geocoding

Finds addresses in Geoapify by coordinates.

```
GET https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/reverse-geocoding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geoapify Geocode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/reverse-geocoding?connectionId=$CONNECTION_ID&lat=52.47944744483806&lon=-1.908554017329216" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "52.47944744483806",
  "lon": "-1.908554017329216"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/reverse-geocoding?${params}`, {
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
| `lat` | number | yes | Latitude coordinate of the target location. Example: `52.47944744483806`. |
| `lon` | number | yes | Longitude coordinate of the target location. Example: `-1.908554017329216`. |
| `type` | list<string> | no | Restrict reverse results to a specific feature type. One of: `amenity`, `city`, `country`, `postcode`, `state`, `street`. Example: `city`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lang` | string | no | Result language using ISO 639-1 code. Example: `en`. |
| `format` | list | no | Response format. One of: `geojson`, `json`, `xml`. Example: `geojson`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "features": [
        {
          "bbox": [
            1
          ],
          "geometry": {
            "coordinates": [
              1
            ],
            "type": "string"
          },
          "properties": {
            "addressLine1": "string",
            "addressLine2": "string",
            "category": "string",
            "city": "string",
            "country": "string",
            "countryCode": "string",
            "county": "string",
            "countyCode": "string",
            "datasource": {
              "attribution": "string",
              "license": "string",
              "sourcename": "Ava Chen",
              "url": "https://example.com"
            },
            "distance": 1,
            "formatted": "string",
            "iso31662": "string",
            "iso31662Sublevel": "string",
            "lat": 1,
            "lon": 1,
            "name": "Ava Chen",
            "placeId": "string",
            "plusCode": "string",
            "plusCodeShort": "string",
            "postcode": "string",
            "rank": {
              "importance": 1,
              "popularity": 1
            },
            "resultType": "string",
            "state": "string",
            "stateCode": "string",
            "street": "string",
            "suburb": "string",
            "timezone": {
              "abbreviationDST": "string",
              "abbreviationSTD": "string",
              "name": "Ava Chen",
              "offsetDST": "string",
              "offsetDSTSeconds": 1,
              "offsetSTD": "string",
              "offsetSTDSeconds": 1
            }
          },
          "type": "string"
        }
      ],
      "query": {
        "lat": 1,
        "lon": 1,
        "plusCode": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features[].bbox[]` | number |  |
| `features[].geometry.coordinates[]` | number |  |
| `features[].geometry.type` | string |  |
| `features[].properties.addressLine1` | string |  |
| `features[].properties.addressLine2` | string |  |
| `features[].properties.category` | string |  |
| `features[].properties.city` | string |  |
| `features[].properties.country` | string |  |
| `features[].properties.countryCode` | string |  |
| `features[].properties.county` | string |  |
| `features[].properties.countyCode` | string |  |
| `features[].properties.datasource.attribution` | string |  |
| `features[].properties.datasource.license` | string |  |
| `features[].properties.datasource.sourcename` | string |  |
| `features[].properties.datasource.url` | string |  |
| `features[].properties.distance` | number |  |
| `features[].properties.formatted` | string |  |
| `features[].properties.iso31662` | string |  |
| `features[].properties.iso31662Sublevel` | string |  |
| `features[].properties.lat` | number |  |
| `features[].properties.lon` | number |  |
| `features[].properties.name` | string |  |
| `features[].properties.placeId` | string |  |
| `features[].properties.plusCode` | string |  |
| `features[].properties.plusCodeShort` | string |  |
| `features[].properties.postcode` | string |  |
| `features[].properties.rank.importance` | number |  |
| `features[].properties.rank.popularity` | number |  |
| `features[].properties.resultType` | string |  |
| `features[].properties.state` | string |  |
| `features[].properties.stateCode` | string |  |
| `features[].properties.street` | string |  |
| `features[].properties.suburb` | string |  |
| `features[].properties.timezone.abbreviationDST` | string |  |
| `features[].properties.timezone.abbreviationSTD` | string |  |
| `features[].properties.timezone.name` | string |  |
| `features[].properties.timezone.offsetDST` | string |  |
| `features[].properties.timezone.offsetDSTSeconds` | number |  |
| `features[].properties.timezone.offsetSTD` | string |  |
| `features[].properties.timezone.offsetSTDSeconds` | number |  |
| `features[].type` | string |  |
| `query.lat` | number |  |
| `query.lon` | number |  |
| `query.plusCode` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Geoapify Geocode API, this operation is `GET /geocode/reverse` (base URL `https://api.geoapify.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-geocoding.md) for the provider-specific parameters and requirements.

