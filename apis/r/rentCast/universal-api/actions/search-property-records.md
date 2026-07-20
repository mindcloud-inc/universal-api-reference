# RentCast: Search Property Records

Finds property records in RentCast by address or area.

```
GET https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/search-property-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RentCast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/search-property-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/search-property-records?${params}`, {
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
| `city` | string | no | City name used to search for property records in a specific city. |
| `state` | string | no | Two-character state abbreviation used to search for property records in a specific state. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Full street address used to search for a specific property or a circular area when paired with radius. |
| `zipCode` | string | no | 5-digit zip code used to search for property records in a specific area. |
| `latitude` | number | no | Latitude of the circular search area when searching by coordinates. |
| `longitude` | number | no | Longitude of the circular search area when searching by coordinates. |
| `radius` | number | no | Radius in miles used with address or coordinates to search within a circular area. |
| `includeTotalCount` | boolean | no | When enabled, RentCast returns the total number of matching property records in the X-Total-Count response header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressLine1": "string",
      "addressLine2": "string",
      "assessorID": "string",
      "bathrooms": 1,
      "bedrooms": 1,
      "city": "string",
      "county": "string",
      "countyFips": "string",
      "features": {},
      "formattedAddress": "string",
      "history": {},
      "id": "string",
      "lastSaleDate": "2026-05-07T12:00:00.000Z",
      "latitude": 1,
      "legalDescription": "string",
      "longitude": 1,
      "lotSize": 1,
      "owner": {},
      "ownerOccupied": true,
      "propertyTaxes": {},
      "propertyType": "string",
      "squareFootage": 1,
      "state": "string",
      "stateFips": "string",
      "subdivision": "string",
      "taxAssessments": {},
      "yearBuilt": 1,
      "zipCode": "string",
      "zoning": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressLine1` | string |  |
| `addressLine2` | string |  |
| `assessorID` | string |  |
| `bathrooms` | number |  |
| `bedrooms` | number |  |
| `city` | string |  |
| `county` | string |  |
| `countyFips` | string |  |
| `features` | object |  |
| `formattedAddress` | string |  |
| `history` | object |  |
| `id` | string |  |
| `lastSaleDate` | date |  |
| `latitude` | number |  |
| `legalDescription` | string |  |
| `longitude` | number |  |
| `lotSize` | number |  |
| `owner` | object |  |
| `ownerOccupied` | boolean |  |
| `propertyTaxes` | object |  |
| `propertyType` | string |  |
| `squareFootage` | number |  |
| `state` | string |  |
| `stateFips` | string |  |
| `subdivision` | string |  |
| `taxAssessments` | object |  |
| `yearBuilt` | number |  |
| `zipCode` | string |  |
| `zoning` | string |  |

## Native endpoint

Through the native RentCast API, this operation is `GET /properties` (base URL `https://api.rentcast.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-property-records.md) for the provider-specific parameters and requirements.

