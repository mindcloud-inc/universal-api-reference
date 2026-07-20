# Ideal Postcodes: Retrieve Address

Retrieves a US address from Ideal Postcodes by address ID.

```
GET https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/retrieve-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ideal Postcodes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/retrieve-address?connectionId=$CONNECTION_ID&address=usps_V118834572%7C310%7C%7C3191" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "usps_V118834572|310||3191"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/retrieve-address?${params}`, {
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
| `address` | string | yes | Address suggestion ID to retrieve in US format. Default: `usps_V118834572\|310\|\|3191`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags` | string | no | Comma-separated tags to associate with the retrieval request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressSecondaryAbbreviation": "string",
      "baseAlternateCode": "string",
      "buildingOrFirmName": "Ava Chen",
      "carrierRouteId": "string",
      "carrierRouteRateSortation": "string",
      "city": "string",
      "cityAbbreviation": "string",
      "cityStateMailingNameIndicator": "ava@example.com",
      "cityStateNameFacilityCode": "Ava Chen",
      "congressionalDistrictNumber": 1,
      "country": "string",
      "countryIso": "string",
      "countryIso2": "string",
      "county": "string",
      "countyNumber": 1,
      "dataset": "string",
      "financeNumber": 1,
      "governmentBuildingIndicator": "string",
      "id": "string",
      "lacsStatusIndicator": "string",
      "language": "string",
      "lastLine": "string",
      "line1": "string",
      "line2": "string",
      "municipalityCityStateKey": "string",
      "plus4Code": "string",
      "preferredCity": "string",
      "preferredLastLineCityStateKey": "string",
      "primaryNumber": "string",
      "recordTypeCode": "string",
      "secondaryNumber": "string",
      "state": "string",
      "stateAbbreviation": "string",
      "streetName": "Ava Chen",
      "streetPostDirectionalAbbreviation": "string",
      "streetPreDirectionalAbbreviation": "string",
      "streetSuffixAbbreviation": "string",
      "updateKeyNumber": "string",
      "urbanizationCityStateKey": "string",
      "zipClassificationCode": "string",
      "zipCode": "string",
      "zipPlus4Code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressSecondaryAbbreviation` | string |  |
| `baseAlternateCode` | string |  |
| `buildingOrFirmName` | string |  |
| `carrierRouteId` | string |  |
| `carrierRouteRateSortation` | string |  |
| `city` | string |  |
| `cityAbbreviation` | string |  |
| `cityStateMailingNameIndicator` | string |  |
| `cityStateNameFacilityCode` | string |  |
| `congressionalDistrictNumber` | number |  |
| `country` | string |  |
| `countryIso` | string |  |
| `countryIso2` | string |  |
| `county` | string |  |
| `countyNumber` | number |  |
| `dataset` | string |  |
| `financeNumber` | number |  |
| `governmentBuildingIndicator` | string |  |
| `id` | string |  |
| `lacsStatusIndicator` | string |  |
| `language` | string |  |
| `lastLine` | string |  |
| `line1` | string |  |
| `line2` | string |  |
| `municipalityCityStateKey` | string |  |
| `plus4Code` | string |  |
| `preferredCity` | string |  |
| `preferredLastLineCityStateKey` | string |  |
| `primaryNumber` | string |  |
| `recordTypeCode` | string |  |
| `secondaryNumber` | string |  |
| `state` | string |  |
| `stateAbbreviation` | string |  |
| `streetName` | string |  |
| `streetPostDirectionalAbbreviation` | string |  |
| `streetPreDirectionalAbbreviation` | string |  |
| `streetSuffixAbbreviation` | string |  |
| `updateKeyNumber` | string |  |
| `urbanizationCityStateKey` | string |  |
| `zipClassificationCode` | string |  |
| `zipCode` | string |  |
| `zipPlus4Code` | string |  |

## Native endpoint

Through the native Ideal Postcodes API, this operation is `GET /autocomplete/addresses/:address/usa` (base URL `https://api.ideal-postcodes.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-address.md) for the provider-specific parameters and requirements.

