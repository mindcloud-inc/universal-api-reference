# List Companies with Zoominfo

Finds companies in ZoomInfo by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `search/company`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [List Companies](https://api-docs.zoominfo.com/#4506f0ad-9147-4016-991f-ce8ef6700f07)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyName` | body | `string` | no | — |
| `companyWebsite` | body | `string` | no | — |
| `companyType` | body | `string` | no | — |
| `companyDescription` | body | `string` | no | — |
| `businessModel[]` | body | `array<string>` | no | — |
| `companyId` | body | `string` | no | — |
| `parentId` | body | `string` | no | — |
| `ultimateParentId` | body | `string` | no | — |
| `sortOrder` | body | `string` | no | — |
| `sortBy` | body | `string` | no | — |
| `companyTicker[]` | body | `array<string>` | no | — |
| `address` | body | `string` | no | — |
| `street` | body | `string` | no | — |
| `state` | body | `string` | no | — |
| `zipCode` | body | `string` | no | — |
| `country` | body | `string` | no | — |
| `continent` | body | `string` | no | — |
| `zipCodeRadiusMiles` | body | `string` | no | — |
| `hashTagString` | body | `string` | no | — |
| `techAttributeTagList` | body | `string` | no | — |
| `subUnitTypes` | body | `string` | no | — |
| `primaryIndustriesOnly` | body | `boolean` | no | — |
| `industryCodes` | body | `string` | no | — |
| `industryKeywords` | body | `string` | no | — |
| `sicCodes` | body | `string` | no | — |
| `naicsCodes` | body | `string` | no | — |
| `revenueMin` | body | `number` | no | — |
| `revenueMax` | body | `number` | no | — |
| `employeeRangeMin` | body | `string` | no | — |
| `employeeRangeMax` | body | `string` | no | — |
| `companyRanking` | body | `string` | no | — |
| `metroRegion` | body | `string` | no | — |
| `locationSearchType` | body | `string` | no | — |
| `fundingAmountMin` | body | `number` | no | — |
| `fundingAmountMax` | body | `number` | no | — |
| `fundingStartDate` | body | `string` | no | — |
| `fundingEndDate` | body | `string` | no | — |
| `zoominfoContactsMin` | body | `string` | no | — |
| `zoominfoContactsMax` | body | `string` | no | — |
| `companyStructureIncludedSubUnitTypes` | body | `string` | no | — |
| `certified` | body | `number` | no | — |
| `excludeDefunctCompanies` | body | `boolean` | no | — |
| `oneYearEmployeeGrowthRateMin` | body | `string` | no | — |
| `oneYearEmployeeGrowthRateMax` | body | `string` | no | — |
| `twoYearEmployeeGrowthRateMin` | body | `string` | no | — |
| `twoYearEmployeeGrowthRateMax` | body | `string` | no | — |
| `engagementStartDate` | body | `string` | no | — |
| `engagementEndDate` | body | `string` | no | — |
| `engagementType[]` | body | `array<string>` | no | — |
| `marketingDepartmentBudgetMin` | body | `number` | no | Minimum marketing department budget amount in thousands. |
| `marketingDepartmentBudgetMax` | body | `number` | no | Maximum marketing department budget amount in thousands. |
| `financeDepartmentBudgetMin` | body | `number` | no | Minimum finance department budget amount in thousands. |
| `financeDepartmentBudgetMax` | body | `number` | no | Maximum finance department budget amount in thousands. |
| `itDepartmentBudgetMin` | body | `number` | no | Minimum IT department budget amount in thousands. |
| `itDepartmentBudgetMax` | body | `number` | no | Maximum IT department budget amount in thousands. |
| `hrDepartmentBudgetMin` | body | `number` | no | Minimum HR department budget amount in thousands. |
| `hrDepartmentBudgetMax` | body | `number` | no | Maximum HR department budget amount in thousands. |
| `includeManagementStatus` | body | `boolean` | no | Return whether records are under management and the purchase date. |
| `revenue` | body | `string` | no | Annual revenue range. |
| `employeeCount` | body | `string` | no | Employee count range. |
