# Geoapify Geocode: Postcode Search

Finds postcodes in Geoapify by location or value.

```
GET https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/postcode-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geoapify Geocode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/postcode-search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/postcode-search?${params}`, {
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
| `postcode` | string | no | Postcode to look up. Example: `SW1A 1AA`. |
| `lat` | number | no | Latitude for nearest postcode search. Example: `51.523767`. |
| `lon` | number | no | Longitude for nearest postcode search. Example: `-0.1585557`. |
| `countryCode` | string | no | ISO 3166-1 alpha-2 country code. Example: `gb`. |
| `geometry` | list | no | Geometry output style. One of: `original`, `point`. Example: `point`. |

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
            "placeId": "string",
            "plusCode": "string",
            "plusCodeShort": "string",
            "postcode": "string",
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
            }
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
| `features[].properties.placeId` | string |  |
| `features[].properties.plusCode` | string |  |
| `features[].properties.plusCodeShort` | string |  |
| `features[].properties.postcode` | string |  |
| `features[].properties.state` | string |  |
| `features[].properties.stateCode` | string |  |
| `features[].properties.timezone.abbreviationDST` | string |  |
| `features[].properties.timezone.abbreviationSTD` | string |  |
| `features[].properties.timezone.name` | string |  |
| `features[].properties.timezone.offsetDST` | string |  |
| `features[].properties.timezone.offsetDSTSeconds` | number |  |
| `features[].properties.timezone.offsetSTD` | string |  |
| `features[].properties.timezone.offsetSTDSeconds` | number |  |
| `features[].type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Geoapify Geocode API, this operation is `GET /postcode/search` (base URL `https://api.geoapify.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/postcode-search.md) for the provider-specific parameters and requirements.

