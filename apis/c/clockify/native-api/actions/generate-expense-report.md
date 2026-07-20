# Generate Expense Report with Clockify

Generates an expense report in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `https://reports.api.clockify.me/v1/workspaces/:workspaceId/reports/expenses/detailed`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Generate Expense Report](https://docs.developer.clockify.me/#tag/Expense-Report/operation/generateDetailedReportV1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `approvalState` | body | `list` | no | Accepted values: `ALL`, `APPROVED`, `UNAPPROVED`. |
| `billable` | body | `boolean` | no | — |
| `categories` | body | `object` | no | — |
| `categories.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `categories.ids[]` | body | `array<string>` | no | — |
| `categories.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `clients` | body | `object` | no | — |
| `clients.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `clients.ids[]` | body | `array<string>` | no | — |
| `clients.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `currency` | body | `object` | no | — |
| `currency.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `currency.ids[]` | body | `array<string>` | no | — |
| `currency.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `dateRangeEnd` | body | `string` | yes | — |
| `dateRangeStart` | body | `string` | yes | — |
| `dateRangeType` | body | `list` | no | Accepted values: `ABSOLUTE`, `LAST_MONTH`, `LAST_WEEK`, `LAST_YEAR`, `PAST_TWO_WEEKS`, `THIS_MONTH`, `THIS_WEEK`, `THIS_YEAR`, `TODAY`, `YESTERDAY`. |
| `exportType` | body | `list` | no | Accepted values: `CSV`, `JSON`, `JSON_V1`, `PDF`, `XLSX`, `ZIP`. |
| `invoicingState` | body | `list` | no | Accepted values: `ALL`, `INVOICED`, `UNINVOICED`. |
| `note` | body | `string` | no | — |
| `page` | body | `number` | no | — |
| `pageSize` | body | `number` | no | — |
| `projects` | body | `object` | no | — |
| `projects.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `projects.ids[]` | body | `array<string>` | no | — |
| `projects.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `sortColumn` | body | `list` | no | Accepted values: `AMOUNT`, `CATEGORY`, `DATE`, `ID`, `PROJECT`, `USER`. |
| `sortOrder` | body | `list` | no | Accepted values: `ASCENDING`, `DESCENDING`. |
| `tasks` | body | `object` | no | — |
| `tasks.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `tasks.ids[]` | body | `array<string>` | no | — |
| `tasks.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `timeZone` | body | `string` | no | — |
| `userGroups` | body | `object` | no | — |
| `userGroups.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userGroups.ids[]` | body | `array<string>` | no | — |
| `userGroups.status` | body | `list` | no | Accepted values: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `userLocale` | body | `string` | no | — |
| `users` | body | `object` | no | — |
| `users.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `users.ids[]` | body | `array<string>` | no | — |
| `users.status` | body | `list` | no | Accepted values: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `weekStart` | body | `list` | no | Accepted values: `FRIDAY`, `MONDAY`, `SATURDAY`, `SUNDAY`, `THURSDAY`, `TUESDAY`, `WEDNESDAY`. |
| `withoutNote` | body | `boolean` | no | — |
| `workspaceId` | path | `list<string>` | yes | — |
| `zoomLevel` | body | `list` | no | Accepted values: `MONTH`, `WEEK`, `YEAR`. |
