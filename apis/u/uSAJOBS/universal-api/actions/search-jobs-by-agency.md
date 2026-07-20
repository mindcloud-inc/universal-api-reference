# USAJOBS: Search Jobs By Agency

Finds jobs in USAJOBS by agency.

```
GET https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/search-jobs-by-agency
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USAJOBS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/search-jobs-by-agency?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/search-jobs-by-agency?${params}`, {
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
| `organization` | string | no | Agency subelement code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "matchedObjectDescriptor": {
        "applicationCloseDate": "string",
        "applyURI": [
          "string"
        ],
        "departmentName": "Ava Chen",
        "jobCategory": [
          {
            "code": "string",
            "name": "Ava Chen"
          }
        ],
        "jobGrade": [
          {
            "code": "string"
          }
        ],
        "organizationName": "Ava Chen",
        "positionEndDate": "string",
        "positionFormattedDescription": [
          {
            "label": "string",
            "labelDescription": "string"
          }
        ],
        "positionID": "string",
        "positionLocation": [
          {
            "cityName": "Ava Chen",
            "countryCode": "string",
            "countrySubDivisionCode": "string",
            "latitude": 1,
            "locationName": "Ava Chen",
            "longitude": 1
          }
        ],
        "positionLocationDisplay": "string",
        "positionOfferingType": [
          {
            "code": "string",
            "name": "Ava Chen"
          }
        ],
        "positionRemuneration": [
          {
            "description": "string",
            "maximumRange": "string",
            "minimumRange": "string",
            "rateIntervalCode": "string"
          }
        ],
        "positionSchedule": [
          {
            "code": "string",
            "name": "Ava Chen"
          }
        ],
        "positionStartDate": "string",
        "positionTitle": "string",
        "positionURI": "string",
        "publicationStartDate": "string",
        "qualificationSummary": "string",
        "userArea": {
          "details": {
            "adjudicationType": [
              "string"
            ],
            "agencyContactEmail": "ava@example.com",
            "agencyContactPhone": "string",
            "agencyMarketingStatement": "string",
            "announcementClosingType": "string",
            "applyOnlineUrl": "https://example.com",
            "bargainingUnitStatus": true,
            "benefits": "string",
            "benefitsDisplayDefaultText": true,
            "commuteDistance": "string",
            "detailStatusUrl": "https://example.com",
            "drugTestRequired": "string",
            "education": "string",
            "evaluations": "string",
            "financialDisclosure": true,
            "highGrade": "string",
            "hiringPath": [
              "string"
            ],
            "howToApply": "string",
            "jobSummary": "string",
            "lowGrade": "string",
            "majorDuties": [
              "string"
            ],
            "organizationCodes": "string",
            "otherInformation": "string",
            "positionSensitivitiy": "string",
            "promotionPotential": "string",
            "relocation": "string",
            "remoteIndicator": true,
            "requiredDocuments": "string",
            "requirements": "string",
            "securityClearance": "string",
            "serviceType": "string",
            "teleworkEligible": true,
            "totalOpenings": "string",
            "travelCode": "string",
            "whatToExpectNext": "string",
            "whoMayApply": {
              "code": "string",
              "name": "Ava Chen"
            },
            "withinArea": "string"
          },
          "isRadialSearch": true
        }
      },
      "matchedObjectId": "string",
      "relevanceRank": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `matchedObjectDescriptor.applicationCloseDate` | string |  |
| `matchedObjectDescriptor.applyURI[]` | string |  |
| `matchedObjectDescriptor.departmentName` | string |  |
| `matchedObjectDescriptor.jobCategory[].code` | string |  |
| `matchedObjectDescriptor.jobCategory[].name` | string |  |
| `matchedObjectDescriptor.jobGrade[].code` | string |  |
| `matchedObjectDescriptor.organizationName` | string |  |
| `matchedObjectDescriptor.positionEndDate` | string |  |
| `matchedObjectDescriptor.positionFormattedDescription[].label` | string |  |
| `matchedObjectDescriptor.positionFormattedDescription[].labelDescription` | string |  |
| `matchedObjectDescriptor.positionID` | string |  |
| `matchedObjectDescriptor.positionLocation[].cityName` | string |  |
| `matchedObjectDescriptor.positionLocation[].countryCode` | string |  |
| `matchedObjectDescriptor.positionLocation[].countrySubDivisionCode` | string |  |
| `matchedObjectDescriptor.positionLocation[].latitude` | number |  |
| `matchedObjectDescriptor.positionLocation[].locationName` | string |  |
| `matchedObjectDescriptor.positionLocation[].longitude` | number |  |
| `matchedObjectDescriptor.positionLocationDisplay` | string |  |
| `matchedObjectDescriptor.positionOfferingType[].code` | string |  |
| `matchedObjectDescriptor.positionOfferingType[].name` | string |  |
| `matchedObjectDescriptor.positionRemuneration[].description` | string |  |
| `matchedObjectDescriptor.positionRemuneration[].maximumRange` | string |  |
| `matchedObjectDescriptor.positionRemuneration[].minimumRange` | string |  |
| `matchedObjectDescriptor.positionRemuneration[].rateIntervalCode` | string |  |
| `matchedObjectDescriptor.positionSchedule[].code` | string |  |
| `matchedObjectDescriptor.positionSchedule[].name` | string |  |
| `matchedObjectDescriptor.positionStartDate` | string |  |
| `matchedObjectDescriptor.positionTitle` | string |  |
| `matchedObjectDescriptor.positionURI` | string |  |
| `matchedObjectDescriptor.publicationStartDate` | string |  |
| `matchedObjectDescriptor.qualificationSummary` | string |  |
| `matchedObjectDescriptor.userArea.details.adjudicationType[]` | string |  |
| `matchedObjectDescriptor.userArea.details.agencyContactEmail` | string |  |
| `matchedObjectDescriptor.userArea.details.agencyContactPhone` | string |  |
| `matchedObjectDescriptor.userArea.details.agencyMarketingStatement` | string |  |
| `matchedObjectDescriptor.userArea.details.announcementClosingType` | string |  |
| `matchedObjectDescriptor.userArea.details.applyOnlineUrl` | string |  |
| `matchedObjectDescriptor.userArea.details.bargainingUnitStatus` | boolean |  |
| `matchedObjectDescriptor.userArea.details.benefits` | string |  |
| `matchedObjectDescriptor.userArea.details.benefitsDisplayDefaultText` | boolean |  |
| `matchedObjectDescriptor.userArea.details.commuteDistance` | string |  |
| `matchedObjectDescriptor.userArea.details.detailStatusUrl` | string |  |
| `matchedObjectDescriptor.userArea.details.drugTestRequired` | string |  |
| `matchedObjectDescriptor.userArea.details.education` | string |  |
| `matchedObjectDescriptor.userArea.details.evaluations` | string |  |
| `matchedObjectDescriptor.userArea.details.financialDisclosure` | boolean |  |
| `matchedObjectDescriptor.userArea.details.highGrade` | string |  |
| `matchedObjectDescriptor.userArea.details.hiringPath[]` | string |  |
| `matchedObjectDescriptor.userArea.details.howToApply` | string |  |
| `matchedObjectDescriptor.userArea.details.jobSummary` | string |  |
| `matchedObjectDescriptor.userArea.details.lowGrade` | string |  |
| `matchedObjectDescriptor.userArea.details.majorDuties[]` | string |  |
| `matchedObjectDescriptor.userArea.details.organizationCodes` | string |  |
| `matchedObjectDescriptor.userArea.details.otherInformation` | string |  |
| `matchedObjectDescriptor.userArea.details.positionSensitivitiy` | string |  |
| `matchedObjectDescriptor.userArea.details.promotionPotential` | string |  |
| `matchedObjectDescriptor.userArea.details.relocation` | string |  |
| `matchedObjectDescriptor.userArea.details.remoteIndicator` | boolean |  |
| `matchedObjectDescriptor.userArea.details.requiredDocuments` | string |  |
| `matchedObjectDescriptor.userArea.details.requirements` | string |  |
| `matchedObjectDescriptor.userArea.details.securityClearance` | string |  |
| `matchedObjectDescriptor.userArea.details.serviceType` | string |  |
| `matchedObjectDescriptor.userArea.details.teleworkEligible` | boolean |  |
| `matchedObjectDescriptor.userArea.details.totalOpenings` | string |  |
| `matchedObjectDescriptor.userArea.details.travelCode` | string |  |
| `matchedObjectDescriptor.userArea.details.whatToExpectNext` | string |  |
| `matchedObjectDescriptor.userArea.details.whoMayApply.code` | string |  |
| `matchedObjectDescriptor.userArea.details.whoMayApply.name` | string |  |
| `matchedObjectDescriptor.userArea.details.withinArea` | string |  |
| `matchedObjectDescriptor.userArea.isRadialSearch` | boolean |  |
| `matchedObjectId` | string |  |
| `relevanceRank` | number |  |

## Native endpoint

Through the native USAJOBS API, this operation is `GET /api/Search` (base URL `https://data.usajobs.gov`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-jobs-by-agency.md) for the provider-specific parameters and requirements.

