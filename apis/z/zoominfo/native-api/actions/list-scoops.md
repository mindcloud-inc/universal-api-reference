# List Scoops with Zoominfo

Finds scoops in ZoomInfo by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `search/scoop`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [List Scoops](https://api-docs.zoominfo.com/#3099d72f-6857-4432-89c2-736410680e60)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publishedStartDate` | body | `string` | no | Starting date to search for scoops based on when published. Form a range using publishedEndDate or omit publishedEndDate to search to the current date. Uses YYYY-MM-DD format. |
| `publishedEndDate` | body | `string` | no | Ending date to search for scoops based on when published. Form a range using publishedEndDate. Uses YYYY-MM-DD format. |
| `updatedSinceCreation` | body | `boolean` | no | Include scoops that have been updated since publishedStartDate |
| `scoopType` | body | `string` | no | Retrieve scoops based on type (e.g. earnings, awards and partnerships). Accepts a comma-separated list of IDs from the endpoint: /lookup/scooptype. |
| `scoopTopic` | body | `string` | no | Retrieve scoops based on topic (e.g. integration, consolidation and compliance). Accepts a comma-separated list of IDs from the endpoint: /lookup/scooptopic. |
| `department` | body | `string` | no | Retrieve scoops based on department (e.g. IT, finance and HR). Accepts a comma-separated list of IDs from the endpoint: /lookup/scoopdepartment. |
| `scoopId` | body | `string` | no | ZoomInfo unique identifier for a scoop. Accepts a comma-separated list. |
| `description` | body | `string` | no | Search for scoops based on description.  Accepts a space-separated list of individual words. |
| `companyTicker` | body | `string` | no | Company stock ticker symbol |
| `companyDescription` | body | `string` | no | Search for companies based on description.  Accepts a space-separated list of individual words. |
| `companyType` | body | `string` | no | Company type (private, public, etc.). Accepts a comma delimited string of types listed in the endpoint: /lookup/companytype Send multiple values as a string separated by `,`. |
| `address` | body | `string` | no | Company address |
| `street` | body | `string` | no | Company street |
| `zipCode` | body | `string` | no | Zip Code of the company's primary address |
| `state` | body | `string` | no | Company state |
| `country` | body | `string` | no | Company country |
| `continent` | body | `string` | no | Company continent |
| `companyId` | body | `string` | no | ZoomInfo unique identifier for the company. Will accept a comma-separated list. |
| `companyName` | body | `string` | no | Company name |
| `companyWebsite` | body | `string` | no | Company domain. Accepts a comma-separated list. |
| `parentId` | body | `string` | no | ZoomInfo Company ID for parent company |
| `ultimateParentId` | body | `string` | no | ZoomInfo Company ID for ultimate parent company |
| `zipCodeRadiusMiles` | body | `string` | no | Used in conjunction with zipCode, designates a geographical radius (in miles) from the zipCode provided. |
| `hashTagString` | body | `string` | no | Hash tags for a company. Can include a comma-separated list. |
| `techAttributeTagList` | body | `string` | no | Specify technology product tags |
| `subUnitTypes` | body | `string` | no | Company sub types (e.g., division, subsidiary) from the endpoint: /lookup/subunittypes. Use this in conjunction with parentId or ultimateParentId. |
| `primaryIndustriesOnly` | body | `boolean` | no | Used in conjunction with the industryCodes input parameter. When set to true, any result returned must have one of the specified industries as a primary industry. If no industries are specified, then this parameter will be ignored. Default is false. |
| `industryCodes` | body | `string` | no | Top-level industry that the contact works in. A contact can have multiple top level industries. Tags are based on the contact's current company. Can include a comma-separated list. |
| `industryKeywords` | body | `string` | no | Industry keywords associated with a company. Can include either 'AND' or 'OR' operators. For example, 'software AND security' or 'software OR security'. |
| `sicCodes` | body | `string` | no | Four-digit numerical codes assigned by the U.S. government to business establishments to identify the primary business of the establishment. Accepts a comma-separated list of values from the endpoint: /lookup/siccode. |
| `naicsCodes` | body | `string` | no | Four-digit numerical codes assigned by the U.S. government to business establishments to identify the primary business of the establishment. Accepts a comma-separated list of values from the endpoint: /lookup/naicscode. |
| `revenue` | body | `string` | no | Annual revenue range in U.S. dollars. Accepts a comma-separated list of values from the endpoint: /lookup/revenuerange. Alternatively, for more granular ranges, you can use the revenueMin and revenueMax parameters. |
| `revenueMin` | body | `number` | no | Minimum annual revenue for a company in U.S. dollars (expressed in thousands). Use with revenueMax to set a range. Alternatively, you can use the revenue parameter to search for pre-defined ranges. |
| `revenueMax` | body | `number` | no | Maximum annual revenue for a company in U.S. dollars (expressed in thousands). Use with revenueMin to set a range. Alternatively, you can use the revenue parameter to search for pre-defined ranges. |
| `employeeRangeMin` | body | `string` | no | Minimum employee count for a company. Use with employeeRangeMax to set a range. Alternatively, you can use the employeeCount parameter to search for pre-defined ranges. |
| `employeeRangeMax` | body | `string` | no | Maximum employee count for a company. Use with employeeRangeMin to set a range. Alternatively, you can use the employeeCount parameter to search for pre-defined ranges. |
| `employeeCount` | body | `string` | no | Employee count range. Accepts a comma-separated list of values from the endpoint: /lookup/employeecount. Alternatively, for more granular ranges, you can use the employeeRangeMin and employeeRangeMax parameters. |
| `companyRanking` | body | `string` | no | Company ranking (e.g., Fortune 500).  Accepts a comma separated list of IDs from the endpoint: /lookup/companyranking. |
| `metroRegion` | body | `string` | no | Company metro area. Accepts a comma-separated list of U.S. and Canada metro areas from the endpoint: /lookup/metroarea. |
| `locationSearchType` | body | `string` | no | Location type (PersonOrHQ, PersonAndHQ, Person, HQ, PersonThenHQ). |
| `fundingAmountMin` | body | `number` | no | Minimum funding amount in thousands (e.g., 1 = 1000, 500 = 500,000). If fundingAmountMin is used without fundingAmountMax, the result will be the amount specified or greater. |
| `fundingAmountMax` | body | `number` | no | Maximum funding amount in thousands (e.g., 1 = 1000, 500 = 500,000). If fundingAmountMax is used without fundingAmountMin, the result will be the amount specified or less. |
| `fundingStartDate` | body | `string` | no | Start date of the funding in YYYY-MM-DD format. If fundingStartDate and fundingEndDate are both specified, they will be used as a range. Start date after end date returns an error. If start date and end date are the same, will return results for exact date. |
| `fundingEndDate` | body | `string` | no | End date of the funding in YYYY-MM-DD format. If fundingStartDate and fundingEndDate are both specified, they will be used as a range. Start date after end date returns an error. If start date and end date are the same, will return results for exact date. |
| `zoominfoContactsMin` | body | `string` | no | Minimum number of ZoomInfo contacts associated with company |
| `zoominfoContactsMax` | body | `string` | no | Maximum number of ZoomInfo contacts associated with company |
| `excludedRegions` | body | `string` | no | Exclude a company state or metro area. Accepts a comma-separated list of U.S. and Canada states and metro areas from the endpoints: /lookup/state and /lookup/metroarea. |
| `companyStructureIncludedSubUnitTypes` | body | `string` | no | Company hierarchical structure |
| `oneYearEmployeeGrowthRateMin` | body | `string` | no | Minimum one year employee growth rate for a company. Use with oneYearEmployeeGrowthRateMax to set a range. |
| `oneYearEmployeeGrowthRateMax` | body | `string` | no | Maximum one year employee growth rate for a company. Use with oneYearEmployeeGrowthRateMin to set a range. |
| `twoYearEmployeeGrowthRateMin` | body | `string` | no | Minimum two year employee growth rate for a company. Use with twoYearEmployeeGrowthRateMax to set a range. |
| `twoYearEmployeeGrowthRateMax` | body | `string` | no | Maximum two year employee growth rate for a company. Use with twoYearEmployeeGrowthRateMin to set a range. |
| `businessModel` | body | `string` | no | Search using Business Model (B2C, B2B, B2G) for a company. Default is All |
| `personId` | body | `string` | no | Unique ZoomInfo identifier for the contact. Can include a comma-separated list. |
| `emailAddress` | body | `string` | no | Work email address for the contact in example@example.com format |
| `hashedEmail` | body | `string` | no | Hashed email value for the contact. Allows searching via an email address with the extra security of not exposing the email. Supported hash algorithms are: MD5, SHA1, SHA256 and SHA512. |
| `fullName` | body | `string` | no | Contact full name |
| `firstName` | body | `string` | no | Contact first name |
| `middleInitial` | body | `string` | no | Contact middle initial |
| `lastName` | body | `string` | no | Contact last name |
| `jobTitle` | body | `string` | no | Contact title at current place of employment. Use OR to input multiple job titles. |
| `excludeJobTitle` | body | `string` | no | Exclude comma-separated list of job titles |
| `managementLevel` | body | `string` | no | Contact management level at current place of employment |
| `excludeManagementLevel` | body | `string` | no | Exclude comma separated list of management levels |
| `boardMember` | body | `string` | no | Exclude or include board members from search results. Values are include, exclude (the default) and only |
| `excludePartialProfiles` | body | `boolean` | no | Contacts who do not have an active company associated with them are considered partial profiles. Exclude contacts with a partial profile from search results. Default is false |
| `executivesOnly` | body | `boolean` | no | Return only executives. Default is false. |
| `requiredFields` | body | `string` | no | Specify a list of required fields for each record returned. Can include email (business email), phone (direct or company phone), directPhone (contact's direct phone), personalEmail, and mobilePhone. Can include a comma-separated list of these fields. |
| `contactAccuracyScoreMin` | body | `string` | no | Minimum accuracy score for search results. This score indicates the likelihood that a contact is reachable and still employed by the company listed. Minimum score is 70 and maximum is 99. |
| `contactAccuracyScoreMax` | body | `string` | no | Maximum accuracy score for search results. This score indicates the likelihood that a contact is reachable and still employed by the company listed. Minimum score is 70 and maximum is 99. |
| `jobFunction` | body | `string` | no | Contact job function at their current place of employment |
| `lastUpdatedInMonths` | body | `number` | no | Number of months within which the contact's profile was last updated |
| `hasBeenNotified` | body | `string` | no | Contacts who have been notified of inclusion in ZoomInfo's database. Values are include (the default), exclude and only |
| `companyPastOrPresent` | body | `string` | no | Returns companies based on a contact's work history. Values are present (default), past and pastAndPresent |
| `school` | body | `string` | no | Searches by contact's education |
| `degree` | body | `string` | no | Searches by contact's education |
| `locationCompanyId` | body | `string` | no | Searches by contact's locationIds |
| `certified` | body | `number` | no | Denotes if ZoomInfo's research and data team has confirmed activity within the past 12 months. 1 = certified, 0 = not certified. |
| `excludeDefunctCompanies` | body | `boolean` | no | Include or exclude defunct companies. The default value is false. |
| `sortBy` | body | `string` | no | Sorts results by valid output fields |
| `sortOrder` | body | `string` | no | Default value is desc. It accepts the following values { asc, ascending, desc, descending |
