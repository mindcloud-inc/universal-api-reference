# List Contacts with Zoominfo

Finds contacts in ZoomInfo by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `search/contact`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [List Contacts](https://api-docs.zoominfo.com/#2e5121fd-df42-41a4-95d6-0e8f24eebd92)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyName` | body | `string` | no | — |
| `companyWebsite` | body | `string` | no | URL to the company website in http://www.example.com format |
| `jobTitle` | body | `string` | no | — |
| `emailAddress` | body | `string` | no | — |
| `firstName` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `middleInitial` | body | `string` | no | — |
| `fullName` | body | `string` | no | — |
| `phone[]` | body | `array<string>` | no | — |
| `revenueMin` | body | `number` | no | — |
| `revenueMax` | body | `number` | no | — |
| `supplementalEmail[]` | body | `array<string>` | no | — |
| `sortOrder` | body | `string` | no | — |
| `sortBy` | body | `string` | no | — |
| `personId` | body | `string` | no | — |
| `excludeJobTitle` | body | `string` | no | — |
| `excludeManagementLevel` | body | `string` | no | — |
| `department` | body | `string` | no | — |
| `excludePartialProfiles` | body | `boolean` | no | Format: `toggle`. |
| `executivesOnly` | body | `boolean` | no | Format: `toggle`. |
| `requiredFields` | body | `string` | no | — |
| `contactAccuracyScoreMin` | body | `string` | no | — |
| `contactAccuracyScoreMax` | body | `string` | no | — |
| `lastUpdatedDateAfter` | body | `string` | no | — |
| `validDateAfter` | body | `string` | no | — |
| `lastUpdatedInMonths` | body | `number` | no | — |
| `hasBeenNotified` | body | `string` | no | — |
| `companyPastOrPresent` | body | `string` | no | — |
| `school` | body | `string` | no | — |
| `degree` | body | `string` | no | — |
| `locationCompanyId[]` | body | `array<string>` | no | — |
| `companyId` | body | `string` | no | — |
| `parentId` | body | `string` | no | — |
| `ultimateParentId` | body | `string` | no | — |
| `hashTagString` | body | `string` | no | — |
| `techAttributeTagList` | body | `string` | no | — |
| `subUnitTypes` | body | `string` | no | — |
| `primaryIndustriesOnly` | body | `boolean` | no | Format: `toggle`. |
| `industryKeywords` | body | `string` | no | — |
| `sicCodes` | body | `string` | no | — |
| `naicsCodes` | body | `string` | no | — |
| `revenue` | body | `string` | no | — |
| `employeeCount` | body | `string` | no | — |
| `companyRanking` | body | `string` | no | — |
| `locationSearchType` | body | `string` | no | — |
| `fundingAmountMin` | body | `number` | no | — |
| `fundingAmountMax` | body | `number` | no | — |
| `fundingStartDate` | body | `string` | no | — |
| `fundingEndDate` | body | `string` | no | — |
| `excludedRegions` | body | `string` | no | — |
| `zoominfoContactsMin` | body | `string` | no | — |
| `zoominfoContactsMax` | body | `string` | no | — |
| `companyStructureIncludedSubUnitTypes` | body | `string` | no | — |
| `oneYearEmployeeGrowthRateMin` | body | `string` | no | — |
| `oneYearEmployeeGrowthRateMax` | body | `string` | no | — |
| `twoYearEmployeeGrowthRateMin` | body | `string` | no | — |
| `twoYearEmployeeGrowthRateMax` | body | `string` | no | — |
| `positionStartDateMin` | body | `string` | no | — |
| `positionStartDateMax` | body | `string` | no | — |
| `webReferences[]` | body | `array<string>` | no | — |
| `engagementType[]` | body | `array<string>` | no | — |
| `buyingGroup[]` | body | `array<string>` | no | Filters results based on the provided Buying Group ID. Only one ID can be submitted. Format: `toggle`. |
| `yearsOfExperience` | body | `string` | no | — |
| `engagementStartDate` | body | `string` | no | — |
| `engagementEndDate` | body | `string` | no | — |
| `jobFunction` | body | `string` | no | — |
| `managementLevel` | body | `string` | no | — |
| `companyType` | body | `string` | no | — |
| `address` | body | `string` | no | — |
| `street` | body | `string` | no | — |
| `metroRegion` | body | `string` | no | — |
| `state` | body | `string` | no | — |
| `zipCode` | body | `string` | no | — |
| `country` | body | `string` | no | — |
| `zipCodeRadiusMiles` | body | `string` | no | — |
| `industryCodes` | body | `string` | no | — |
| `employeeRangeMin` | body | `string` | no | — |
| `employeeRangeMax` | body | `string` | no | — |
| `hashedEmail` | body | `string` | no | Hashed email value for the contact. |
| `boardMember` | body | `string` | no | Include or exclude board members from search results. |
| `exactJobTitle` | body | `string` | no | Exact-match job title at the contact's current company. |
| `includeManagementStatus` | body | `boolean` | no | Return whether records are under management and the purchase date. |
| `companyTicker[]` | body | `array<string>` | no | Company stock ticker symbol. |
| `companyDescription` | body | `string` | no | Search for companies based on description. |
| `continent` | body | `string` | no | Company continent. |
| `employeeCount` | body | `string` | no | Employee count range. |
| `excludedRegions` | body | `string` | no | Exclude company state or metro area values. |
