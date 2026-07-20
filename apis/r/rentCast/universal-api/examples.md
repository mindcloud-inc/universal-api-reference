# RentCast Universal API Examples

These examples use the MindCloud API key and RentCast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Random Property Records

Retrieves random property records from RentCast.

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

Example response:

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

See the full [List Random Property Records action reference](actions/list-random-property-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rentCast/latest/actions/list-random-property-records).
