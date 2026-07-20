# Zoominfo: List Contacts

Finds contacts in ZoomInfo by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-contacts?${params}`, {
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
| `companyName` | string | no |  |
| `companyWebsite` | string | no | URL to the company website in http://www.example.com format |
| `jobTitle` | string | no |  |
| `emailAddress` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `middleInitial` | string | no |  |
| `fullName` | string | no |  |
| `phone[]` | array<string> | no |  |
| `revenueMin` | number | no |  |
| `revenueMax` | number | no |  |
| `supplementalEmail[]` | array<string> | no |  |
| `sortOrder` | string | no |  |
| `sortBy` | string | no |  |
| `personId` | string | no |  |
| `excludeJobTitle` | string | no |  |
| `excludeManagementLevel` | string | no |  |
| `department` | string | no |  |
| `excludePartialProfiles` | boolean | no |  |
| `executivesOnly` | boolean | no |  |
| `requiredFields` | string | no |  |
| `contactAccuracyScoreMin` | string | no |  |
| `contactAccuracyScoreMax` | string | no |  |
| `lastUpdatedDateAfter` | string | no |  |
| `validDateAfter` | string | no |  |
| `lastUpdatedInMonths` | number | no |  |
| `hasBeenNotified` | string | no |  |
| `companyPastOrPresent` | string | no |  |
| `school` | string | no |  |
| `degree` | string | no |  |
| `locationCompanyId[]` | array<string> | no |  |
| `companyId` | string | no |  |
| `parentId` | string | no |  |
| `ultimateParentId` | string | no |  |
| `hashTagString` | string | no |  |
| `techAttributeTagList` | string | no |  |
| `subUnitTypes` | string | no |  |
| `primaryIndustriesOnly` | boolean | no |  |
| `industryKeywords` | string | no |  |
| `sicCodes` | string | no |  |
| `naicsCodes` | string | no |  |
| `revenue` | string | no |  |
| `employeeCount` | string | no |  |
| `companyRanking` | string | no |  |
| `locationSearchType` | string | no |  |
| `fundingAmountMin` | number | no |  |
| `fundingAmountMax` | number | no |  |
| `fundingStartDate` | string | no |  |
| `fundingEndDate` | string | no |  |
| `excludedRegions` | string | no |  |
| `zoominfoContactsMin` | string | no |  |
| `zoominfoContactsMax` | string | no |  |
| `companyStructureIncludedSubUnitTypes` | string | no |  |
| `oneYearEmployeeGrowthRateMin` | string | no |  |
| `oneYearEmployeeGrowthRateMax` | string | no |  |
| `twoYearEmployeeGrowthRateMin` | string | no |  |
| `twoYearEmployeeGrowthRateMax` | string | no |  |
| `positionStartDateMin` | string | no |  |
| `positionStartDateMax` | string | no |  |
| `webReferences[]` | array<string> | no |  |
| `engagementType[]` | array<string> | no |  |
| `buyingGroup[]` | array<string> | no | Filters results based on the provided Buying Group ID. Only one ID can be submitted. |
| `yearsOfExperience` | string | no |  |
| `engagementStartDate` | string | no |  |
| `engagementEndDate` | string | no |  |
| `jobFunction` | string | no |  |
| `managementLevel` | string | no |  |
| `companyType` | string | no |  |
| `address` | string | no |  |
| `street` | string | no |  |
| `metroRegion` | string | no |  |
| `state` | string | no |  |
| `zipCode` | string | no |  |
| `country` | string | no |  |
| `zipCodeRadiusMiles` | string | no |  |
| `industryCodes` | string | no |  |
| `employeeRangeMin` | string | no |  |
| `employeeRangeMax` | string | no |  |
| `hashedEmail` | string | no | Hashed email value for the contact. |
| `boardMember` | string | no | Include or exclude board members from search results. |
| `exactJobTitle` | string | no | Exact-match job title at the contact's current company. |
| `includeManagementStatus` | boolean | no | Return whether records are under management and the purchase date. |
| `companyTicker[]` | array<string> | no | Company stock ticker symbol. |
| `companyDescription` | string | no | Search for companies based on description. |
| `continent` | string | no | Company continent. |
| `employeeCount` | string | no | Employee count range. |
| `excludedRegions` | string | no | Exclude company state or metro area values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "id": 1,
        "name": "Ava Chen"
      },
      "contactAccuracyScore": 1,
      "directPhoneDoNotCall": true,
      "firstName": "Ava",
      "hasCompanyCountry": true,
      "hasCompanyEmployeeCount": true,
      "hasCompanyIndustry": true,
      "hasCompanyPhone": true,
      "hasCompanyRevenue": true,
      "hasCompanyState": true,
      "hasCompanyStreet": true,
      "hasCompanyZipCode": true,
      "hasDirectPhone": true,
      "hasEmail": true,
      "hasMobilePhone": true,
      "hasSupplementalEmail": true,
      "id": 1,
      "jobTitle": "string",
      "lastName": "Chen",
      "lastUpdatedDate": "string",
      "middleName": "Ava Chen",
      "mobilePhoneDoNotCall": true,
      "validDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.id` | number |  |
| `company.name` | string |  |
| `contactAccuracyScore` | number |  |
| `directPhoneDoNotCall` | boolean |  |
| `firstName` | string |  |
| `hasCompanyCountry` | boolean |  |
| `hasCompanyEmployeeCount` | boolean |  |
| `hasCompanyIndustry` | boolean |  |
| `hasCompanyPhone` | boolean |  |
| `hasCompanyRevenue` | boolean |  |
| `hasCompanyState` | boolean |  |
| `hasCompanyStreet` | boolean |  |
| `hasCompanyZipCode` | boolean |  |
| `hasDirectPhone` | boolean |  |
| `hasEmail` | boolean |  |
| `hasMobilePhone` | boolean |  |
| `hasSupplementalEmail` | boolean |  |
| `id` | number |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `lastUpdatedDate` | string |  |
| `middleName` | string |  |
| `mobilePhoneDoNotCall` | boolean |  |
| `validDate` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST search/contact` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

