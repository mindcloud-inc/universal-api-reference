# RentCast: List Random Property Records

Retrieves random property records from RentCast.

```
GET https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/list-random-property-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RentCast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/list-random-property-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/list-random-property-records?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native RentCast API, this operation is `GET /properties/random` (base URL `https://api.rentcast.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-random-property-records.md) for the provider-specific parameters and requirements.

