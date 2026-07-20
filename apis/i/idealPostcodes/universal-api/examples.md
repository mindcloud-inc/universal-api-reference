# Ideal Postcodes Universal API Examples

These examples use the MindCloud API key and Ideal Postcodes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Lookup Postcode

Retrieves addresses from Ideal Postcodes for a UK postcode.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/lookup-postcode?connectionId=$CONNECTION_ID&postcode=SW1A%202AA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postcode": "SW1A 2AA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/lookup-postcode?${params}`, {
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
      "administrativeCounty": "string",
      "buildingName": "Ava Chen",
      "buildingNumber": "string",
      "country": "string",
      "countryIso": "string",
      "countryIso2": "string",
      "county": "string",
      "countyCode": "string",
      "dataset": "string",
      "deliveryPointSuffix": "string",
      "departmentName": "Ava Chen",
      "dependantLocality": "string",
      "dependantThoroughfare": "string",
      "district": "string",
      "doubleDependantLocality": "string",
      "eastings": 1,
      "id": "string",
      "language": "string",
      "latitude": 1,
      "line1": "string",
      "line2": "string",
      "line3": "string",
      "longitude": 1,
      "northings": 1,
      "organisationName": "Ava Chen",
      "poBox": "string",
      "postalCounty": "string",
      "postcode": "string",
      "postcodeInward": "string",
      "postcodeOutward": "string",
      "postcodeType": "string",
      "postTown": "string",
      "premise": "string",
      "subBuildingName": "Ava Chen",
      "suOrganisationIndicator": "string",
      "thoroughfare": "string",
      "traditionalCounty": "string",
      "udprn": 1,
      "umprn": "string",
      "uprn": "string",
      "ward": "string"
    }
  ],
  "meta": {}
}
```

See the full [Lookup Postcode action reference](actions/lookup-postcode.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/idealPostcodes/latest/actions/lookup-postcode).
