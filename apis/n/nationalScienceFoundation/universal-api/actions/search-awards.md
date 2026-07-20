# National Science Foundation: Search Awards

Finds awards in National Science Foundation by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/nationalScienceFoundation/latest/actions/search-awards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a National Science Foundation `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalScienceFoundation/latest/actions/search-awards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalScienceFoundation/latest/actions/search-awards?${params}`, {
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
| `keyword` | string | no | Free-text search across all available award data. Boolean operators AND, OR, and NOT are supported by the NSF API. Example: `water`. |
| `activeAwards` | boolean | no | Set to true to include active awards. |
| `expiredAwards` | boolean | no | Set to true to include expired awards. |
| `awardeeName` | string | no | Name of the entity receiving the award. Example: `university of south florida`. |
| `pdPIName` | string | no | Project Director or Principal Investigator name. Example: `SUMNET STARFIELD`. |
| `poName` | string | no | NSF program officer name. Example: `Hamos Rick`. |
| `fundProgramName` | string | no | NSF fund program name. Example: `ANTARCTIC COORDINATION`. |
| `cfdaNumber` | string | no | Catalog of Federal Domestic Assistance number, such as 47.084. Example: `47.084`. |
| `awardeeStateCode` | string | no | Awardee state abbreviation, such as VA. Example: `VA`. |
| `awardeeCountryCode` | string | no | Awardee country code, such as US. Example: `US`. |
| `perfLocation` | string | no | Performance location name. Example: `university of south florida`. |
| `perfStateCode` | string | no | Performance state abbreviation, such as VA. Example: `VA`. |
| `dateStart` | string | no | Start date for award date search. NSF expects mm/dd/yyyy, such as 12/31/2012. Example: `12/31/2012`. |
| `dateEnd` | string | no | End date for award date search. NSF expects mm/dd/yyyy, such as 12/31/2012. Example: `12/31/2012`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `progEleCode` | string | no | NSF program element code, a six-digit PEC such as 999300. Example: `999300`. |
| `progRefCode` | string | no | NSF program reference code. |
| `orgCodeDir` | string | no | Directorate organization code, an eight-digit code such as 15000000. Example: `15000000`. |
| `orgCodeDiv` | string | no | Division organization code, an eight-digit code such as 15030000. Example: `15030000`. |
| `startDateStart` | string | no | Start date for award start date search. NSF expects mm/dd/yyyy. Example: `12/31/2012`. |
| `startDateEnd` | string | no | End date for award start date search. NSF expects mm/dd/yyyy. Example: `12/31/2012`. |
| `expDateStart` | string | no | Start date for award expiration date search. NSF expects mm/dd/yyyy. Example: `12/31/2012`. |
| `expDateEnd` | string | no | End date for award expiration date search. NSF expects mm/dd/yyyy. Example: `12/31/2012`. |
| `estimatedTotalAmtFrom` | number | no | Return awards greater than this estimated total amount. Example: `50000`. |
| `estimatedTotalAmtTo` | number | no | Return awards less than this estimated total amount. Example: `500000`. |
| `fundsObligatedAmtFrom` | number | no | Return awards greater than this obligated amount. Example: `50000`. |
| `fundsObligatedAmtTo` | number | no | Return awards less than this obligated amount. Example: `500000`. |
| `transType` | string | no | Award transaction type, such as Standard Grant, Continuing Grant, Cooperative Agreement, or Fellowship Award. Example: `Standard Grant`. |
| `ueiNumber` | string | no | Unique Entity Identifier, such as F2VSMAKDH8Z7. Example: `F2VSMAKDH8Z7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abstractText": "string",
      "activeAwd": "string",
      "agency": "string",
      "awardAgencyCode": "string",
      "awardee": "string",
      "awardeeAddress": "string",
      "awardeeCity": "string",
      "awardeeCountryCode": "string",
      "awardeeDistrict": "string",
      "awardeeDistrictCode": "string",
      "awardeeName": "Ava Chen",
      "awardeePhone": "string",
      "awardeeStateCode": "string",
      "awardeeZipCode": "string",
      "cfdaNumber": "string",
      "date": "string",
      "dirAbbr": "string",
      "divAbbr": "string",
      "estimatedTotalAmt": "string",
      "expDate": "string",
      "fundAgencyCode": "string",
      "fundProgramName": "Ava Chen",
      "fundsObligated": [
        "string"
      ],
      "fundsObligatedAmt": "string",
      "histAwd": "string",
      "id": "string",
      "initAmendmentDate": "string",
      "latestAmendmentDate": "string",
      "managingPec": "string",
      "orgCodeDir": "string",
      "orgCodeDiv": "string",
      "orgLongName": "Ava Chen",
      "orgLongName2": "Ava Chen",
      "orgUrl": "https://example.com",
      "parentUeiNumber": "string",
      "pdPIName": "Ava Chen",
      "perfAddress": "string",
      "perfCity": "string",
      "perfCountryCode": "string",
      "perfDistrict": "string",
      "perfDistrictCode": "string",
      "perfLocation": "string",
      "perfStateCode": "string",
      "perfZipCode": "string",
      "pi": [
        "string"
      ],
      "piEmail": "ava@example.com",
      "piFirstName": "Ava",
      "piLastName": "Chen",
      "piMiddeInitial": "string",
      "poEmail": "ava@example.com",
      "poName": "Ava Chen",
      "poPhone": "string",
      "primaryProgram": [
        "string"
      ],
      "progEleCode": "string",
      "program": "string",
      "progRefCode": "string",
      "projectOutComesReport": "string",
      "publicAccessMandate": "string",
      "startDate": "string",
      "title": "string",
      "transType": "string",
      "ueiNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abstractText` | string |  |
| `activeAwd` | string |  |
| `agency` | string |  |
| `awardAgencyCode` | string |  |
| `awardee` | string |  |
| `awardeeAddress` | string |  |
| `awardeeCity` | string |  |
| `awardeeCountryCode` | string |  |
| `awardeeDistrict` | string |  |
| `awardeeDistrictCode` | string |  |
| `awardeeName` | string |  |
| `awardeePhone` | string |  |
| `awardeeStateCode` | string |  |
| `awardeeZipCode` | string |  |
| `cfdaNumber` | string |  |
| `date` | string |  |
| `dirAbbr` | string |  |
| `divAbbr` | string |  |
| `estimatedTotalAmt` | string |  |
| `expDate` | string |  |
| `fundAgencyCode` | string |  |
| `fundProgramName` | string |  |
| `fundsObligated` | array<string> |  |
| `fundsObligatedAmt` | string |  |
| `histAwd` | string |  |
| `id` | string |  |
| `initAmendmentDate` | string |  |
| `latestAmendmentDate` | string |  |
| `managingPec` | string |  |
| `orgCodeDir` | string |  |
| `orgCodeDiv` | string |  |
| `orgLongName` | string |  |
| `orgLongName2` | string |  |
| `orgUrl` | string |  |
| `parentUeiNumber` | string |  |
| `pdPIName` | string |  |
| `perfAddress` | string |  |
| `perfCity` | string |  |
| `perfCountryCode` | string |  |
| `perfDistrict` | string |  |
| `perfDistrictCode` | string |  |
| `perfLocation` | string |  |
| `perfStateCode` | string |  |
| `perfZipCode` | string |  |
| `pi` | array<string> |  |
| `piEmail` | string |  |
| `piFirstName` | string |  |
| `piLastName` | string |  |
| `piMiddeInitial` | string |  |
| `poEmail` | string |  |
| `poName` | string |  |
| `poPhone` | string |  |
| `primaryProgram` | array<string> |  |
| `progEleCode` | string |  |
| `program` | string |  |
| `progRefCode` | string |  |
| `projectOutComesReport` | string |  |
| `publicAccessMandate` | string |  |
| `startDate` | string |  |
| `title` | string |  |
| `transType` | string |  |
| `ueiNumber` | string |  |

## Native endpoint

Through the native National Science Foundation API, this operation is `GET /awards.json` (base URL `https://api.nsf.gov/services/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-awards.md) for the provider-specific parameters and requirements.

