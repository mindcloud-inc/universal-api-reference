# USAJOBS Universal API Examples

These examples use the MindCloud API key and USAJOBS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Developer Jobs

Finds developer job postings in USAJOBS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/search-developer-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/search-developer-jobs?${params}`, {
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
        "subAgency": "string",
        "userArea": {
          "details": {
            "adjudicationType": [
              "string"
            ],
            "agencyContactEmail": "ava@example.com",
            "agencyMarketingStatement": "string",
            "announcementClosingType": "string",
            "applyOnlineUrl": "https://example.com",
            "bargainingUnitStatus": true,
            "benefits": "string",
            "benefitsDisplayDefaultText": true,
            "benefitsUrl": "https://example.com",
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
            "mCOTags": [
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
            "subAgencyName": "Ava Chen",
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

See the full [Search Developer Jobs action reference](actions/search-developer-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uSAJOBS/latest/actions/search-developer-jobs).
