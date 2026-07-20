# Loqate: Lookup UK Government Data By Postcode

Retrieves UK government data from Loqate by postcode.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/lookup-uk-government-data-by-postcode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/lookup-uk-government-data-by-postcode?connectionId=$CONNECTION_ID&postcode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postcode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/lookup-uk-government-data-by-postcode?${params}`, {
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
| `postcode` | string | yes | The postcode to search with. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cCGAreaCode": "string",
      "cCGAreaName": "Ava Chen",
      "cCGCode": "string",
      "cCGName": "Ava Chen",
      "cCGRegionCode": "string",
      "cCGRegionName": "Ava Chen",
      "countryCode": "string",
      "countryName": "Ava Chen",
      "countyCode": "string",
      "countyName": "Ava Chen",
      "districtCode": "string",
      "districtName": "Ava Chen",
      "easting": 1,
      "governmentOfficeCode": "string",
      "governmentOfficeName": "Ava Chen",
      "latitude": 1,
      "leaCode": "string",
      "leaName": "Ava Chen",
      "longitude": 1,
      "lSOACode": "string",
      "lSOAName": "Ava Chen",
      "mSOACode": "string",
      "mSOAName": "Ava Chen",
      "newCountryCode": "string",
      "newCountyCode": "string",
      "newDistrictCode": "string",
      "newNhsPctCode": "string",
      "newNhsShaCode": "string",
      "newWardCode": "string",
      "nhsPctCode": "string",
      "nhsPctName": "Ava Chen",
      "nhsShaCode": "string",
      "nhsShaName": "Ava Chen",
      "northing": 1,
      "osGrid": "string",
      "wardCode": "string",
      "wardName": "Ava Chen",
      "westminsterConstituencyCode": "string",
      "westminsterConstituencyCode2010": "string",
      "westminsterConstituencyName": "Ava Chen",
      "westminsterConstituencyName2010": "Ava Chen",
      "westminsterMP": "string",
      "westminsterParty": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cCGAreaCode` | string |  |
| `cCGAreaName` | string |  |
| `cCGCode` | string |  |
| `cCGName` | string |  |
| `cCGRegionCode` | string |  |
| `cCGRegionName` | string |  |
| `countryCode` | string |  |
| `countryName` | string |  |
| `countyCode` | string |  |
| `countyName` | string |  |
| `districtCode` | string |  |
| `districtName` | string |  |
| `easting` | number |  |
| `governmentOfficeCode` | string |  |
| `governmentOfficeName` | string |  |
| `latitude` | number |  |
| `leaCode` | string |  |
| `leaName` | string |  |
| `longitude` | number |  |
| `lSOACode` | string |  |
| `lSOAName` | string |  |
| `mSOACode` | string |  |
| `mSOAName` | string |  |
| `newCountryCode` | string |  |
| `newCountyCode` | string |  |
| `newDistrictCode` | string |  |
| `newNhsPctCode` | string |  |
| `newNhsShaCode` | string |  |
| `newWardCode` | string |  |
| `nhsPctCode` | string |  |
| `nhsPctName` | string |  |
| `nhsShaCode` | string |  |
| `nhsShaName` | string |  |
| `northing` | number |  |
| `osGrid` | string |  |
| `wardCode` | string |  |
| `wardName` | string |  |
| `westminsterConstituencyCode` | string |  |
| `westminsterConstituencyCode2010` | string |  |
| `westminsterConstituencyName` | string |  |
| `westminsterConstituencyName2010` | string |  |
| `westminsterMP` | string |  |
| `westminsterParty` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /GovernmentData/Postzon/RetrieveByPostcode/v1.50/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-uk-government-data-by-postcode.md) for the provider-specific parameters and requirements.

