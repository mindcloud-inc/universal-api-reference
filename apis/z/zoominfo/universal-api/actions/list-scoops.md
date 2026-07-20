# Zoominfo: List Scoops

Finds scoops in ZoomInfo by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-scoops
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-scoops?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-scoops?${params}`, {
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
| `publishedStartDate` | string | no | Starting date to search for scoops based on when published. Form a range using publishedEndDate or omit publishedEndDate to search to the current date. Uses YYYY-MM-DD format. |
| `publishedEndDate` | string | no | Ending date to search for scoops based on when published. Form a range using publishedEndDate. Uses YYYY-MM-DD format. |
| `updatedSinceCreation` | boolean | no | Include scoops that have been updated since publishedStartDate |
| `scoopType` | string | no | Retrieve scoops based on type (e.g. earnings, awards and partnerships). Accepts a comma-separated list of IDs from the endpoint: /lookup/scooptype. |
| `scoopTopic` | string | no | Retrieve scoops based on topic (e.g. integration, consolidation and compliance). Accepts a comma-separated list of IDs from the endpoint: /lookup/scooptopic. |
| `department` | string | no | Retrieve scoops based on department (e.g. IT, finance and HR). Accepts a comma-separated list of IDs from the endpoint: /lookup/scoopdepartment. |
| `scoopId` | string | no | ZoomInfo unique identifier for a scoop. Accepts a comma-separated list. |
| `description` | string | no | Search for scoops based on description. Accepts a space-separated list of individual words. |
| `companyTicker` | string | no | Company stock ticker symbol |
| `companyDescription` | string | no | Search for companies based on description. Accepts a space-separated list of individual words. |
| `companyType` | string | no | Company type (private, public, etc.). Accepts a comma delimited string of types listed in the endpoint: /lookup/companytype Accepts multiple values in one string, delimited by `,`. |
| `address` | string | no | Company address |
| `street` | string | no | Company street |
| `zipCode` | string | no | Zip Code of the company's primary address |
| `state` | string | no | Company state |
| `country` | string | no | Company country |
| `continent` | string | no | Company continent |
| `companyId` | string | no | ZoomInfo unique identifier for the company. Will accept a comma-separated list. |
| `companyName` | string | no | Company name |
| `companyWebsite` | string | no | Company domain. Accepts a comma-separated list. |
| `parentId` | string | no | ZoomInfo Company ID for parent company |
| `ultimateParentId` | string | no | ZoomInfo Company ID for ultimate parent company |
| `zipCodeRadiusMiles` | string | no | Used in conjunction with zipCode, designates a geographical radius (in miles) from the zipCode provided. |
| `hashTagString` | string | no | Hash tags for a company. Can include a comma-separated list. |
| `techAttributeTagList` | string | no | Specify technology product tags |
| `subUnitTypes` | string | no | Company sub types (e.g., division, subsidiary) from the endpoint: /lookup/subunittypes. Use this in conjunction with parentId or ultimateParentId. |
| `primaryIndustriesOnly` | boolean | no | Used in conjunction with the industryCodes input parameter. When set to true, any result returned must have one of the specified industries as a primary industry. If no industries are specified, then this parameter will be ignored. Default is false. |
| `industryCodes` | string | no | Top-level industry that the contact works in. A contact can have multiple top level industries. Tags are based on the contact's current company. Can include a comma-separated list. |
| `industryKeywords` | string | no | Industry keywords associated with a company. Can include either 'AND' or 'OR' operators. For example, 'software AND security' or 'software OR security'. |
| `sicCodes` | string | no | Four-digit numerical codes assigned by the U.S. government to business establishments to identify the primary business of the establishment. Accepts a comma-separated list of values from the endpoint: /lookup/siccode. |
| `naicsCodes` | string | no | Four-digit numerical codes assigned by the U.S. government to business establishments to identify the primary business of the establishment. Accepts a comma-separated list of values from the endpoint: /lookup/naicscode. |
| `revenue` | string | no | Annual revenue range in U.S. dollars. Accepts a comma-separated list of values from the endpoint: /lookup/revenuerange. Alternatively, for more granular ranges, you can use the revenueMin and revenueMax parameters. |
| `revenueMin` | number | no | Minimum annual revenue for a company in U.S. dollars (expressed in thousands). Use with revenueMax to set a range. Alternatively, you can use the revenue parameter to search for pre-defined ranges. |
| `revenueMax` | number | no | Maximum annual revenue for a company in U.S. dollars (expressed in thousands). Use with revenueMin to set a range. Alternatively, you can use the revenue parameter to search for pre-defined ranges. |
| `employeeRangeMin` | string | no | Minimum employee count for a company. Use with employeeRangeMax to set a range. Alternatively, you can use the employeeCount parameter to search for pre-defined ranges. |
| `employeeRangeMax` | string | no | Maximum employee count for a company. Use with employeeRangeMin to set a range. Alternatively, you can use the employeeCount parameter to search for pre-defined ranges. |
| `employeeCount` | string | no | Employee count range. Accepts a comma-separated list of values from the endpoint: /lookup/employeecount. Alternatively, for more granular ranges, you can use the employeeRangeMin and employeeRangeMax parameters. |
| `companyRanking` | string | no | Company ranking (e.g., Fortune 500). Accepts a comma separated list of IDs from the endpoint: /lookup/companyranking. |
| `metroRegion` | string | no | Company metro area. Accepts a comma-separated list of U.S. and Canada metro areas from the endpoint: /lookup/metroarea. |
| `locationSearchType` | string | no | Location type (PersonOrHQ, PersonAndHQ, Person, HQ, PersonThenHQ). |
| `fundingAmountMin` | number | no | Minimum funding amount in thousands (e.g., 1 = 1000, 500 = 500,000). If fundingAmountMin is used without fundingAmountMax, the result will be the amount specified or greater. |
| `fundingAmountMax` | number | no | Maximum funding amount in thousands (e.g., 1 = 1000, 500 = 500,000). If fundingAmountMax is used without fundingAmountMin, the result will be the amount specified or less. |
| `fundingStartDate` | string | no | Start date of the funding in YYYY-MM-DD format. If fundingStartDate and fundingEndDate are both specified, they will be used as a range. Start date after end date returns an error. If start date and end date are the same, will return results for exact date. |
| `fundingEndDate` | string | no | End date of the funding in YYYY-MM-DD format. If fundingStartDate and fundingEndDate are both specified, they will be used as a range. Start date after end date returns an error. If start date and end date are the same, will return results for exact date. |
| `zoominfoContactsMin` | string | no | Minimum number of ZoomInfo contacts associated with company |
| `zoominfoContactsMax` | string | no | Maximum number of ZoomInfo contacts associated with company |
| `excludedRegions` | string | no | Exclude a company state or metro area. Accepts a comma-separated list of U.S. and Canada states and metro areas from the endpoints: /lookup/state and /lookup/metroarea. |
| `companyStructureIncludedSubUnitTypes` | string | no | Company hierarchical structure |
| `oneYearEmployeeGrowthRateMin` | string | no | Minimum one year employee growth rate for a company. Use with oneYearEmployeeGrowthRateMax to set a range. |
| `oneYearEmployeeGrowthRateMax` | string | no | Maximum one year employee growth rate for a company. Use with oneYearEmployeeGrowthRateMin to set a range. |
| `twoYearEmployeeGrowthRateMin` | string | no | Minimum two year employee growth rate for a company. Use with twoYearEmployeeGrowthRateMax to set a range. |
| `twoYearEmployeeGrowthRateMax` | string | no | Maximum two year employee growth rate for a company. Use with twoYearEmployeeGrowthRateMin to set a range. |
| `businessModel` | string | no | Search using Business Model (B2C, B2B, B2G) for a company. Default is All |
| `personId` | string | no | Unique ZoomInfo identifier for the contact. Can include a comma-separated list. |
| `emailAddress` | string | no | Work email address for the contact in example@example.com format |
| `hashedEmail` | string | no | Hashed email value for the contact. Allows searching via an email address with the extra security of not exposing the email. Supported hash algorithms are: MD5, SHA1, SHA256 and SHA512. |
| `fullName` | string | no | Contact full name |
| `firstName` | string | no | Contact first name |
| `middleInitial` | string | no | Contact middle initial |
| `lastName` | string | no | Contact last name |
| `jobTitle` | string | no | Contact title at current place of employment. Use OR to input multiple job titles. |
| `excludeJobTitle` | string | no | Exclude comma-separated list of job titles |
| `managementLevel` | string | no | Contact management level at current place of employment |
| `excludeManagementLevel` | string | no | Exclude comma separated list of management levels |
| `boardMember` | string | no | Exclude or include board members from search results. Values are include, exclude (the default) and only |
| `excludePartialProfiles` | boolean | no | Contacts who do not have an active company associated with them are considered partial profiles. Exclude contacts with a partial profile from search results. Default is false |
| `executivesOnly` | boolean | no | Return only executives. Default is false. |
| `requiredFields` | string | no | Specify a list of required fields for each record returned. Can include email (business email), phone (direct or company phone), directPhone (contact's direct phone), personalEmail, and mobilePhone. Can include a comma-separated list of these fields. |
| `contactAccuracyScoreMin` | string | no | Minimum accuracy score for search results. This score indicates the likelihood that a contact is reachable and still employed by the company listed. Minimum score is 70 and maximum is 99. |
| `contactAccuracyScoreMax` | string | no | Maximum accuracy score for search results. This score indicates the likelihood that a contact is reachable and still employed by the company listed. Minimum score is 70 and maximum is 99. |
| `jobFunction` | string | no | Contact job function at their current place of employment |
| `lastUpdatedInMonths` | number | no | Number of months within which the contact's profile was last updated |
| `hasBeenNotified` | string | no | Contacts who have been notified of inclusion in ZoomInfo's database. Values are include (the default), exclude and only |
| `companyPastOrPresent` | string | no | Returns companies based on a contact's work history. Values are present (default), past and pastAndPresent |
| `school` | string | no | Searches by contact's education |
| `degree` | string | no | Searches by contact's education |
| `locationCompanyId` | string | no | Searches by contact's locationIds |
| `certified` | number | no | Denotes if ZoomInfo's research and data team has confirmed activity within the past 12 months. 1 = certified, 0 = not certified. |
| `excludeDefunctCompanies` | boolean | no | Include or exclude defunct companies. The default value is false. |
| `sortBy` | string | no | Sorts results by valid output fields |
| `sortOrder` | string | no | Default value is desc. It accepts the following values { asc, ascending, desc, descending |

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
      "description": "string",
      "id": 1,
      "link": "https://example.com",
      "linkText": "https://example.com",
      "originalPublishedDate": "string",
      "person": {
        "contacts": [
          "string"
        ]
      },
      "publishedDate": "string",
      "topics": [
        "string"
      ],
      "types": [
        {}
      ],
      "updateText": "string"
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
| `description` | string |  |
| `id` | number |  |
| `link` | string |  |
| `linkText` | string |  |
| `originalPublishedDate` | string |  |
| `person.contacts` | array<string> |  |
| `publishedDate` | string |  |
| `topics` | array<string> |  |
| `types` | array<object> |  |
| `updateText` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST search/scoop` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-scoops.md) for the provider-specific parameters and requirements.

