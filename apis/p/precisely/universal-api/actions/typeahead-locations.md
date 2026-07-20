# Precisely: Typeahead Locations

Finds address suggestions in Precisely by partial location input.

```
GET https://connect.mindcloud.co/v1/universal/precisely/latest/actions/typeahead-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Precisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/typeahead-locations?connectionId=$CONNECTION_ID&searchText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/precisely/latest/actions/typeahead-locations?${params}`, {
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
| `searchText` | string | yes | The partial address text to search for. |
| `country` | string | no | ISO country code to search within. |
| `latitude` | number | no | The latitude of the reference location. |
| `longitude` | number | no | The longitude of the reference location. |
| `ipAddress` | string | no | IP address used to detect a search location when coordinates are not supplied. |
| `areaName1` | string | no | Largest geographic area, typically a state or province. |
| `areaName3` | string | no | City or town name used with country filtering. |
| `postCode` | string | no | Postal code used with country filtering. |
| `maxCandidates` | number | no | Maximum number of address suggestions to return. |
| `searchRadius` | number | no | Radius to search within around the reference location. |
| `searchRadiusUnit` | string | no | Unit for the search radius. |
| `autoDetectLocation` | string | no | Whether to auto-detect location from the IP address. |
| `returnAdminAreasOnly` | string | no | Whether to return only admin-area matches. |
| `searchOnAddressNumber` | string | no | Whether to prefer matching on address number. |
| `includeRangesDetails` | string | no | Whether to include ranges and unit details in the response. |
| `searchOnUnitInfo` | string | no | Whether to search unit information such as apartment or house number. |
| `searchOnPOBox` | string | no | Whether to include PO Box matches in the search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "addressLastLine": "string",
        "addressNumber": "string",
        "areaName1": "Ava Chen",
        "areaName3": "Ava Chen",
        "country": "string",
        "formattedAddress": "string",
        "mainAddressLine": "string",
        "placeName": "Ava Chen",
        "postCode": "string",
        "streetName": "Ava Chen"
      },
      "geometry": {
        "coordinates": [
          1
        ],
        "type": "string"
      },
      "ranges": [
        {}
      ],
      "totalUnitCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.addressLastLine` | string | City, state, and postal line. |
| `address.addressNumber` | string | Address number. |
| `address.areaName1` | string | Top-level administrative area, typically state or province. |
| `address.areaName3` | string | City or locality name. |
| `address.country` | string | ISO country code. |
| `address.formattedAddress` | string | Fully formatted candidate address. |
| `address.mainAddressLine` | string | Primary street-address line. |
| `address.placeName` | string | Place or venue name when available. |
| `address.postCode` | string | Postal code. |
| `address.streetName` | string | Street name. |
| `geometry.coordinates` | array<number> | Longitude and latitude coordinates. |
| `geometry.type` | string | GeoJSON geometry type. |
| `ranges` | array<object> | Unit or range details returned for the candidate. |
| `totalUnitCount` | number | Count of units or ranges returned for the candidate. |

## Native endpoint

Through the native Precisely API, this operation is `GET /typeahead/v1/locations` (base URL `https://api.precisely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/typeahead-locations.md) for the provider-specific parameters and requirements.

