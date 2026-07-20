# Geoapify Geocode: Postcode List

Retrieves a filtered list of postcodes from Geoapify.

```
GET https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/postcode-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geoapify Geocode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/postcode-list?connectionId=$CONNECTION_ID&text=OX" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "OX"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/postcode-list?${params}`, {
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
| `text` | string | yes | Autocomplete text for postcode and locality names. Example: `OX`. |
| `countryCode` | string | no | ISO 3166-1 alpha-2 country code. Example: `gb`. |
| `geometry` | list | no | Geometry output style. One of: `original`, `point`. Example: `point`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Restrict search area using rectangle, circle, place, or countrycode syntax. Example: `countrycode:gb`. |
| `bias` | string | no | Prioritize results near a region or point. Example: `proximity:-1.2616996,51.750242`. |
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
            "city": "string",
            "country": "string",
            "countryCode": "string",
            "county": "string",
            "datasource": {
              "attribution": "string",
              "license": "string",
              "sourcename": "Ava Chen",
              "url": "https://example.com"
            },
            "formatted": "string",
            "iso31662": "string",
            "iso31662Sublevel": "string",
            "lat": 1,
            "lon": 1,
            "municipality": "string",
            "parentAsPlaceId": true,
            "placeId": "string",
            "plusCode": "string",
            "postcode": "string",
            "resultType": "string",
            "state": "string",
            "stateCode": "string",
            "timezone": {
              "abbreviationDST": "string",
              "abbreviationSTD": "string",
              "name": "Ava Chen",
              "offsetDST": "string",
              "offsetDSTSeconds": 1,
              "offsetSTD": "string",
              "offsetSTDSeconds": 1
            },
            "town": "string"
          },
          "type": "string"
        }
      ],
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
| `features[].properties.city` | string |  |
| `features[].properties.country` | string |  |
| `features[].properties.countryCode` | string |  |
| `features[].properties.county` | string |  |
| `features[].properties.datasource.attribution` | string |  |
| `features[].properties.datasource.license` | string |  |
| `features[].properties.datasource.sourcename` | string |  |
| `features[].properties.datasource.url` | string |  |
| `features[].properties.formatted` | string |  |
| `features[].properties.iso31662` | string |  |
| `features[].properties.iso31662Sublevel` | string |  |
| `features[].properties.lat` | number |  |
| `features[].properties.lon` | number |  |
| `features[].properties.municipality` | string |  |
| `features[].properties.parentAsPlaceId` | boolean |  |
| `features[].properties.placeId` | string |  |
| `features[].properties.plusCode` | string |  |
| `features[].properties.postcode` | string |  |
| `features[].properties.resultType` | string |  |
| `features[].properties.state` | string |  |
| `features[].properties.stateCode` | string |  |
| `features[].properties.timezone.abbreviationDST` | string |  |
| `features[].properties.timezone.abbreviationSTD` | string |  |
| `features[].properties.timezone.name` | string |  |
| `features[].properties.timezone.offsetDST` | string |  |
| `features[].properties.timezone.offsetDSTSeconds` | number |  |
| `features[].properties.timezone.offsetSTD` | string |  |
| `features[].properties.timezone.offsetSTDSeconds` | number |  |
| `features[].properties.town` | string |  |
| `features[].type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Geoapify Geocode API, this operation is `GET /postcode/list` (base URL `https://api.geoapify.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/postcode-list.md) for the provider-specific parameters and requirements.

