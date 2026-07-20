# Geoapify Geocode: Address Autocomplete

Finds address and place suggestions in Geoapify.

```
GET https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/address-autocomplete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geoapify Geocode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/address-autocomplete?connectionId=$CONNECTION_ID&text=1600%20Pennsylvania%20Ave%20NW" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "1600 Pennsylvania Ave NW"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/address-autocomplete?${params}`, {
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
| `text` | string | yes | Free-form address or place text to autocomplete. Example: `1600 Pennsylvania Ave NW`. |
| `type` | list<string> | no | Restrict suggestions to specific location types. One of: `amenity`, `city`, `country`, `locality`, `postcode`, `state`, `street`. Example: `city`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Restrict search area using rectangle, circle, place, or countrycode syntax. Example: `countrycode:us`. |
| `bias` | string | no | Prioritize results near a region or point. Example: `proximity:-77.0365,38.8977`. |
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
              "confidenceStreetLevel": 1,
              "importance": 1,
              "matchType": "string"
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
        "parsed": {
          "expectedType": "string",
          "housenumber": "string",
          "street": "string"
        },
        "text": "string"
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
| `features[].properties.city` | string |  |
| `features[].properties.country` | string |  |
| `features[].properties.countryCode` | string |  |
| `features[].properties.datasource.attribution` | string |  |
| `features[].properties.datasource.license` | string |  |
| `features[].properties.datasource.sourcename` | string |  |
| `features[].properties.datasource.url` | string |  |
| `features[].properties.district` | string |  |
| `features[].properties.formatted` | string |  |
| `features[].properties.housenumber` | string |  |
| `features[].properties.iso31662` | string |  |
| `features[].properties.lat` | number |  |
| `features[].properties.lon` | number |  |
| `features[].properties.name` | string |  |
| `features[].properties.placeId` | string |  |
| `features[].properties.plusCode` | string |  |
| `features[].properties.postcode` | string |  |
| `features[].properties.rank.confidence` | number |  |
| `features[].properties.rank.confidenceBuildingLevel` | number |  |
| `features[].properties.rank.confidenceStreetLevel` | number |  |
| `features[].properties.rank.importance` | number |  |
| `features[].properties.rank.matchType` | string |  |
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
| `query.parsed.expectedType` | string |  |
| `query.parsed.housenumber` | string |  |
| `query.parsed.street` | string |  |
| `query.text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Geoapify Geocode API, this operation is `GET /geocode/autocomplete` (base URL `https://api.geoapify.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/address-autocomplete.md) for the provider-specific parameters and requirements.

