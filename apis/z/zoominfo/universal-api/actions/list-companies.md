# Zoominfo: List Companies

Finds companies in ZoomInfo by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-companies?${params}`, {
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
| `companyWebsite` | string | no |  |
| `companyType` | string | no |  |
| `companyDescription` | string | no |  |
| `businessModel[]` | array<string> | no |  |
| `companyId` | string | no |  |
| `parentId` | string | no |  |
| `ultimateParentId` | string | no |  |
| `sortOrder` | string | no |  |
| `sortBy` | string | no |  |
| `companyTicker[]` | array<string> | no |  |
| `address` | string | no |  |
| `street` | string | no |  |
| `state` | string | no |  |
| `zipCode` | string | no |  |
| `country` | string | no |  |
| `continent` | string | no |  |
| `zipCodeRadiusMiles` | string | no |  |
| `hashTagString` | string | no |  |
| `techAttributeTagList` | string | no |  |
| `subUnitTypes` | string | no |  |
| `primaryIndustriesOnly` | boolean | no |  |
| `industryCodes` | string | no |  |
| `industryKeywords` | string | no |  |
| `sicCodes` | string | no |  |
| `naicsCodes` | string | no |  |
| `revenueMin` | number | no |  |
| `revenueMax` | number | no |  |
| `employeeRangeMin` | string | no |  |
| `employeeRangeMax` | string | no |  |
| `companyRanking` | string | no |  |
| `metroRegion` | string | no |  |
| `locationSearchType` | string | no |  |
| `fundingAmountMin` | number | no |  |
| `fundingAmountMax` | number | no |  |
| `fundingStartDate` | string | no |  |
| `fundingEndDate` | string | no |  |
| `zoominfoContactsMin` | string | no |  |
| `zoominfoContactsMax` | string | no |  |
| `companyStructureIncludedSubUnitTypes` | string | no |  |
| `certified` | number | no |  |
| `excludeDefunctCompanies` | boolean | no |  |
| `oneYearEmployeeGrowthRateMin` | string | no |  |
| `oneYearEmployeeGrowthRateMax` | string | no |  |
| `twoYearEmployeeGrowthRateMin` | string | no |  |
| `twoYearEmployeeGrowthRateMax` | string | no |  |
| `engagementStartDate` | string | no |  |
| `engagementEndDate` | string | no |  |
| `engagementType[]` | array<string> | no |  |
| `marketingDepartmentBudgetMin` | number | no | Minimum marketing department budget amount in thousands. |
| `marketingDepartmentBudgetMax` | number | no | Maximum marketing department budget amount in thousands. |
| `financeDepartmentBudgetMin` | number | no | Minimum finance department budget amount in thousands. |
| `financeDepartmentBudgetMax` | number | no | Maximum finance department budget amount in thousands. |
| `itDepartmentBudgetMin` | number | no | Minimum IT department budget amount in thousands. |
| `itDepartmentBudgetMax` | number | no | Maximum IT department budget amount in thousands. |
| `hrDepartmentBudgetMin` | number | no | Minimum HR department budget amount in thousands. |
| `hrDepartmentBudgetMax` | number | no | Maximum HR department budget amount in thousands. |
| `includeManagementStatus` | boolean | no | Return whether records are under management and the purchase date. |
| `revenue` | string | no | Annual revenue range. |
| `employeeCount` | string | no | Employee count range. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST search/company` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

