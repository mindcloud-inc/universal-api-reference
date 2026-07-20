# RentCast: Get Sale Listing by ID

Retrieves a sale listing from RentCast by ID.

```
GET https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/get-sale-listing-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RentCast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/get-sale-listing-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/get-sale-listing-by-id?${params}`, {
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
| `id` | string | yes | The RentCast sale listing ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressLine1": "string",
      "addressLine2": "string",
      "bathrooms": 1,
      "bedrooms": 1,
      "city": "string",
      "county": "string",
      "countyFips": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "daysOnMarket": 1,
      "formattedAddress": "string",
      "history": {},
      "id": "string",
      "lastSeenDate": "2026-05-07T12:00:00.000Z",
      "latitude": 1,
      "listedDate": "2026-05-07T12:00:00.000Z",
      "listingAgent": {},
      "listingOffice": {},
      "listingType": "string",
      "longitude": 1,
      "lotSize": 1,
      "mlsName": "Ava Chen",
      "mlsNumber": "string",
      "price": 1,
      "propertyType": "string",
      "removedDate": "2026-05-07T12:00:00.000Z",
      "squareFootage": 1,
      "state": "string",
      "stateFips": "string",
      "status": "string",
      "yearBuilt": 1,
      "zipCode": "string"
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
| `bathrooms` | number |  |
| `bedrooms` | number |  |
| `city` | string |  |
| `county` | string |  |
| `countyFips` | string |  |
| `createdDate` | date |  |
| `daysOnMarket` | number |  |
| `formattedAddress` | string |  |
| `history` | object |  |
| `id` | string |  |
| `lastSeenDate` | date |  |
| `latitude` | number |  |
| `listedDate` | date |  |
| `listingAgent` | object |  |
| `listingOffice` | object |  |
| `listingType` | string |  |
| `longitude` | number |  |
| `lotSize` | number |  |
| `mlsName` | string |  |
| `mlsNumber` | string |  |
| `price` | number |  |
| `propertyType` | string |  |
| `removedDate` | date |  |
| `squareFootage` | number |  |
| `state` | string |  |
| `stateFips` | string |  |
| `status` | string |  |
| `yearBuilt` | number |  |
| `zipCode` | string |  |

## Native endpoint

Through the native RentCast API, this operation is `GET /listings/sale/:id` (base URL `https://api.rentcast.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sale-listing-by-id.md) for the provider-specific parameters and requirements.

