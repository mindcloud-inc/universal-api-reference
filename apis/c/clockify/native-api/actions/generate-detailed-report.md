# Generate Detailed Report with Clockify

Generates a detailed report in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `https://reports.api.clockify.me/v1/workspaces/:workspaceId/reports/detailed`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Generate Detailed Report](https://docs.developer.clockify.me/#tag/Time-Entry-Report/operation/generateDetailedReport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amounts` | body | `list<string>` | no | Accepted values: `COST`, `EARNED`, `EXPORT`, `HIDE_AMOUNT`, `PROFIT`. Send multiple values as a array. |
| `amountShown` | body | `list<string>` | no | Accepted values: `COST`, `EARNED`, `EXPORT`, `HIDE_AMOUNT`, `PROFIT`. |
| `approvalState` | body | `list<string>` | no | Accepted values: `ALL`, `APPROVED`, `UNAPPROVED`. |
| `archived` | body | `boolean` | no | — |
| `attendanceFilter` | body | `object` | no | — |
| `attendanceFilter.breakFilters[]` | body | `array<object>` | no | — |
| `attendanceFilter.breakFilters[].filtrationType` | body | `list<string>` | no | Accepted values: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.breakFilters[].value` | body | `string` | no | — |
| `attendanceFilter.capacityFilters[]` | body | `array<object>` | no | — |
| `attendanceFilter.capacityFilters[].filtrationType` | body | `list<string>` | no | Accepted values: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.capacityFilters[].value` | body | `string` | no | — |
| `attendanceFilter.endFilters[]` | body | `array<object>` | no | — |
| `attendanceFilter.endFilters[].filtrationType` | body | `list<string>` | no | Accepted values: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.endFilters[].value` | body | `string` | no | — |
| `attendanceFilter.hasTimeOff` | body | `boolean` | no | — |
| `attendanceFilter.overtimeFilters[]` | body | `array<object>` | no | — |
| `attendanceFilter.overtimeFilters[].filtrationType` | body | `list<string>` | no | Accepted values: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.overtimeFilters[].value` | body | `string` | no | — |
| `attendanceFilter.page` | body | `number` | no | — |
| `attendanceFilter.pageSize` | body | `number` | no | — |
| `attendanceFilter.sortColumn` | body | `list<string>` | no | Accepted values: `BREAK`, `CAPACITY`, `DATE`, `END`, `OVERTIME`, `START`, `TIME_OFF`, `USER`, `WORK`. |
| `attendanceFilter.startFilters[]` | body | `array<object>` | no | — |
| `attendanceFilter.startFilters[].filtrationType` | body | `list<string>` | no | Accepted values: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.startFilters[].value` | body | `string` | no | — |
| `attendanceFilter.workFilters[]` | body | `array<object>` | no | — |
| `attendanceFilter.workFilters[].filtrationType` | body | `list<string>` | no | Accepted values: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.workFilters[].value` | body | `string` | no | — |
| `billable` | body | `boolean` | no | — |
| `clients` | body | `object` | no | — |
| `clients.contains` | body | `list<string>` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `clients.ids[]` | body | `array<string>` | no | — |
| `clients.status` | body | `list<string>` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `currency` | body | `object` | no | — |
| `currency.contains` | body | `list<string>` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `currency.ids[]` | body | `array<string>` | no | — |
| `currency.status` | body | `list<string>` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `customFields[]` | body | `array<object>` | no | — |
| `customFields[].id` | body | `string` | no | — |
| `customFields[].isEmpty` | body | `boolean` | no | — |
| `customFields[].numberCondition` | body | `list<string>` | no | Accepted values: `EQUAL`, `GREATER_THAN`, `LESS_THAN`. |
| `customFields[].type` | body | `list<string>` | no | Accepted values: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. |
| `customFields[].value` | body | `object` | no | — |
| `dateFormat` | body | `string` | no | — |
| `dateRangeType` | body | `list<string>` | no | Accepted values: `ABSOLUTE`, `LAST_MONTH`, `LAST_WEEK`, `LAST_YEAR`, `PAST_TWO_WEEKS`, `THIS_MONTH`, `THIS_WEEK`, `THIS_YEAR`, `TODAY`, `YESTERDAY`. |
| `description` | body | `string` | no | — |
| `detailedFilter.auditFilter` | body | `object` | no | — |
| `detailedFilter.auditFilter.duration` | body | `number` | no | — |
| `detailedFilter.auditFilter.durationShorter` | body | `boolean` | no | — |
| `detailedFilter.auditFilter.withoutProject` | body | `boolean` | no | — |
| `detailedFilter.auditFilter.withoutTask` | body | `boolean` | no | — |
| `detailedFilter.options` | body | `object` | no | — |
| `detailedFilter.options.totals` | body | `list<string>` | no | Accepted values: `CALCULATE`, `EXCLUDE`. |
| `exportType` | body | `list<string>` | no | Accepted values: `CSV`, `JSON`, `JSON_V1`, `PDF`, `XLSX`, `ZIP`. |
| `invoicingState` | body | `list<string>` | no | Accepted values: `ALL`, `INVOICED`, `UNINVOICED`. |
| `projects` | body | `object` | no | — |
| `projects.contains` | body | `list<string>` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `projects.ids[]` | body | `array<string>` | no | — |
| `projects.status` | body | `list<string>` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `rounding` | body | `boolean` | no | — |
| `sortOrder` | body | `list<string>` | no | Accepted values: `ASCENDING`, `DESCENDING`. |
| `summaryFilter` | body | `object` | no | — |
| `summaryFilter.groups[]` | body | `array<string>` | no | — |
| `summaryFilter.sortColumn` | body | `list<string>` | no | Accepted values: `AMOUNT`, `COST`, `DURATION`, `EARNED`, `GROUP`, `PROFIT`. |
| `summaryFilter.summaryChartType` | body | `list<string>` | no | Accepted values: `BILLABILITY`, `PROJECT`. |
| `tags` | body | `object` | no | — |
| `tags.containedInTimeentry` | body | `list<string>` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `tags.contains` | body | `list<string>` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `tags.ids[]` | body | `array<string>` | no | — |
| `tags.status` | body | `list<string>` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `tasks` | body | `object` | no | — |
| `tasks.contains` | body | `list<string>` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `tasks.ids[]` | body | `array<string>` | no | — |
| `tasks.status` | body | `list<string>` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `timeFormat` | body | `string` | no | — |
| `timeZone` | body | `string` | no | — |
| `userCustomFields[]` | body | `array<object>` | no | — |
| `userCustomFields[].id` | body | `string` | no | — |
| `userCustomFields[].isEmpty` | body | `boolean` | no | — |
| `userCustomFields[].numberCondition` | body | `list<string>` | no | Accepted values: `EQUAL`, `GREATER_THAN`, `LESS_THAN`. |
| `userCustomFields[].type` | body | `list<string>` | no | Accepted values: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. |
| `userCustomFields[].value` | body | `object` | no | — |
| `userGroups` | body | `object` | no | — |
| `userGroups.contains` | body | `list<string>` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userGroups.ids[]` | body | `array<string>` | no | — |
| `userGroups.status` | body | `list<string>` | no | Accepted values: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `userLocale` | body | `string` | no | — |
| `users` | body | `object` | no | — |
| `users.contains` | body | `list<string>` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `users.ids[]` | body | `array<string>` | no | — |
| `users.status` | body | `list<string>` | no | Accepted values: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `weeklyFilter` | body | `object` | no | — |
| `weeklyFilter.group` | body | `string` | no | — |
| `weeklyFilter.subgroup` | body | `string` | no | — |
| `weekStart` | body | `list<string>` | no | Accepted values: `FRIDAY`, `MONDAY`, `SATURDAY`, `SUNDAY`, `THURSDAY`, `TUESDAY`, `WEDNESDAY`. |
| `withoutDescription` | body | `boolean` | no | — |
| `workspaceId` | path | `list<string>` | yes | — |
| `zoomLevel` | body | `list<string>` | no | Accepted values: `MONTH`, `WEEK`, `YEAR`. |
| `dateRangeStart` | body | `string` | yes | — |
| `dateRangeEnd` | body | `string` | yes | — |
| `detailedFilter` | body | `object` | yes | — |
| `detailedFilter.page` | body | `number` | no | — |
| `detailedFilter.pageSize` | body | `number` | no | — |
| `detailedFilter.sortColumn` | body | `list<string>` | no | Accepted values: `DATE`, `DESCRIPTION`, `DURATION`, `ID`, `NATURAL`, `USER`, `USER_DATE`, `ZONED_DATE`. |
