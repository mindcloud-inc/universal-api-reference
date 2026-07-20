# <img src="https://images.mindcloud.co/apps/icons/department-of-agriculture_1776364716773.png" alt="Department of Agriculture logo" width="28" height="28"> Department of Agriculture: Universal API

Access USDA Economic Research Service Agricultural Resource Management Survey data, including states, years, reports, variables, farm types, categories, and survey result records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/departmentOfAgriculture/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ers.usda.gov/
- **Vendor API docs:** https://www.ers.usda.gov/developer/data-apis/arms-data-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List ARMS States](actions/list-arms-states.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-states?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Arms Category

| Action | Method | Description |
| --- | --- | --- |
| [List ARMS Categories](actions/list-arms-categories.md) | GET | Retrieves ARMS categories from Department of Agriculture. |
| [Search ARMS Categories](actions/search-arms-categories.md) | GET | Finds ARMS categories in Department of Agriculture by ID or name. |

### Arms Farm Type

| Action | Method | Description |
| --- | --- | --- |
| [List ARMS Farm Types](actions/list-arms-farm-types.md) | GET | Retrieves ARMS farm types from Department of Agriculture. |
| [Search ARMS Farm Types](actions/search-arms-farm-types.md) | GET | Finds ARMS farm types in Department of Agriculture by ID or name. |

### Arms Report

| Action | Method | Description |
| --- | --- | --- |
| [List ARMS Reports](actions/list-arms-reports.md) | GET | Retrieves ARMS reports from Department of Agriculture. |
| [Search ARMS Reports](actions/search-arms-reports.md) | GET | Finds ARMS reports in Department of Agriculture by ID or name. |

### Arms Survey Data

| Action | Method | Description |
| --- | --- | --- |
| [Get ARMS Survey Data](actions/get-arms-survey-data.md) | GET | Retrieves ARMS survey data from Department of Agriculture. |
| [Get ARMS Survey Data by Report](actions/get-arms-survey-data-by-report.md) | GET | Retrieves ARMS survey data by report from Department of Agriculture. |
| [Get Farm Business Balance Sheet Survey Data](actions/get-farm-business-balance-sheet-survey-data.md) | GET | Retrieves Farm Business Balance Sheet survey data from Department of Agriculture. |
| [Get Farm Business Debt Repayment Capacity Survey Data](actions/get-farm-business-debt-repayment-capacity-survey-data.md) | GET | Retrieves Farm Business Debt Repayment Capacity survey data from Department of Agriculture. |
| [Get Farm Business Financial Ratios Survey Data](actions/get-farm-business-financial-ratios-survey-data.md) | GET | Retrieves Farm Business Financial Ratios survey data from Department of Agriculture. |
| [Get Farm Business Income Statement Survey Data](actions/get-farm-business-income-statement-survey-data.md) | GET | Retrieves Farm Business Income Statement survey data from Department of Agriculture. |
| [Get Government Payments Survey Data](actions/get-government-payments-survey-data.md) | GET | Retrieves Government Payments survey data from Department of Agriculture. |
| [Get Operator Household Balance Sheet Survey Data](actions/get-operator-household-balance-sheet-survey-data.md) | GET | Retrieves Operator Household Balance Sheet survey data from Department of Agriculture. |
| [Get Operator Household Income Survey Data](actions/get-operator-household-income-survey-data.md) | GET | Retrieves Operator Household Income survey data from Department of Agriculture. |
| [Get Structural Characteristics Survey Data](actions/get-structural-characteristics-survey-data.md) | GET | Retrieves Structural Characteristics survey data from Department of Agriculture. |

### Arms Variable

| Action | Method | Description |
| --- | --- | --- |
| [List ARMS Variables](actions/list-arms-variables.md) | GET | Retrieves ARMS variables from Department of Agriculture. |
| [Search ARMS Variables](actions/search-arms-variables.md) | GET | Finds ARMS variables in Department of Agriculture by ID, name, report, or group. |

### Arms Year

| Action | Method | Description |
| --- | --- | --- |
| [List ARMS Years](actions/list-arms-years.md) | GET | Retrieves ARMS survey years from Department of Agriculture. |

### State

| Action | Method | Description |
| --- | --- | --- |
| [List ARMS States](actions/list-arms-states.md) | GET | Retrieves ARMS states from Department of Agriculture. |

