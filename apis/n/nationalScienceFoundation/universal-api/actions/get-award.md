# National Science Foundation: Get Award

Retrieves award information from National Science Foundation by ID.

```
GET https://connect.mindcloud.co/v1/universal/nationalScienceFoundation/latest/actions/get-award
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a National Science Foundation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalScienceFoundation/latest/actions/get-award?connectionId=$CONNECTION_ID&id=1052893" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1052893"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalScienceFoundation/latest/actions/get-award?${params}`, {
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
| `id` | string | yes | Award unique identifier, such as 1052893. Example: `1052893`. |

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

Through the native National Science Foundation API, this operation is `GET /awards/[:id].json` (base URL `https://api.nsf.gov/services/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-award.md) for the provider-specific parameters and requirements.

