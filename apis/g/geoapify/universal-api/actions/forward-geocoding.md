# Geoapify Geocode: Forward Geocoding

Finds locations in Geoapify by address.

```
GET https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/forward-geocoding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geoapify Geocode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/forward-geocoding?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/forward-geocoding?${params}`, {
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
| `name` | string | no | Amenity or place name Example: `Starbucks`. |
| `text` | string | no | Free-form address or place name to geocode Example: `1600 Pennsylvania Ave NW, Washington, DC`. |
| `houseNumber` | string | no | Structured address house number Example: `1600`. |
| `street` | string | no | Structured address street name Example: `Pennsylvania Ave NW`. |
| `postcode` | string | no | Structured address postcode or ZIP code Example: `20500`. |
| `city` | string | no | Structured address city name Example: `Washington`. |
| `state` | string | no | Structured address state or region name Example: `District of Columbia`. |
| `country` | string | no | Structured address country name Example: `United States`. |
| `type` | list<string> | no | Limit results to a location type such as country, state, city, postcode, street, or amenity One of: `amenity`, `city`, `country`, `locality`, `postcode`, `state`, `street`. Example: `city`. |
| `lang` | string | no | Result language using ISO 639-1 code Example: `en`. |
| `filter` | string | no | Restrict search area using circle, rectangle, countrycode, or place filter syntax Example: `countrycode:us`. |
| `bias` | string | no | Prioritize results near a region or point without strict filtering Example: `proximity:-77.0365,38.8977`. |
| `format` | list | no | Response format: geojson (default), json, or xml One of: `geojson`, `json`, `xml`. Example: `geojson`. |

## Response

```json
{
  "success": true,
  "data": [
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
        "city": "Ava Chen",
        "country": "string",
        "countryCode": "string",
        "datasource": {
          "attribution": "string",
          "license": "string",
          "sourcename": "Ava Chen",
          "url": "https://example.com"
        },
        "district": "string",
        "formatted": "string",
        "housenumber": "string",
        "iso31662": "string",
        "lat": 1,
        "lon": 1,
        "name": "Ava Chen",
        "placeId": "string",
        "plusCode": "string",
        "postcode": "string",
        "rank": {
          "confidence": 1,
          "confidenceBuildingLevel": 1,
          "confidenceCityLevel": 1,
          "confidenceStreetLevel": 1,
          "importance": 1,
          "matchType": "string",
          "popularity": 1
        },
        "resultType": "string",
        "state": "string",
        "stateCode": "string",
        "street": "Ava Chen",
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bbox[]` | number |  |
| `geometry.coordinates[]` | number |  |
| `geometry.type` | string |  |
| `properties.addressLine1` | string |  |
| `properties.addressLine2` | string |  |
| `properties.city` | string |  |
| `properties.country` | string |  |
| `properties.countryCode` | string |  |
| `properties.datasource.attribution` | string |  |
| `properties.datasource.license` | string |  |
| `properties.datasource.sourcename` | string |  |
| `properties.datasource.url` | string |  |
| `properties.district` | string |  |
| `properties.formatted` | string |  |
| `properties.housenumber` | string |  |
| `properties.iso31662` | string |  |
| `properties.lat` | number |  |
| `properties.lon` | number |  |
| `properties.name` | string |  |
| `properties.placeId` | string |  |
| `properties.plusCode` | string |  |
| `properties.postcode` | string |  |
| `properties.rank.confidence` | number |  |
| `properties.rank.confidenceBuildingLevel` | number |  |
| `properties.rank.confidenceCityLevel` | number |  |
| `properties.rank.confidenceStreetLevel` | number |  |
| `properties.rank.importance` | number |  |
| `properties.rank.matchType` | string |  |
| `properties.rank.popularity` | number |  |
| `properties.resultType` | string |  |
| `properties.state` | string |  |
| `properties.stateCode` | string |  |
| `properties.street` | string |  |
| `properties.suburb` | string |  |
| `properties.timezone.abbreviationDST` | string |  |
| `properties.timezone.abbreviationSTD` | string |  |
| `properties.timezone.name` | string |  |
| `properties.timezone.offsetDST` | string |  |
| `properties.timezone.offsetDSTSeconds` | number |  |
| `properties.timezone.offsetSTD` | string |  |
| `properties.timezone.offsetSTDSeconds` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Geoapify Geocode API, this operation is `GET /geocode/search` (base URL `https://api.geoapify.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/forward-geocoding.md) for the provider-specific parameters and requirements.

