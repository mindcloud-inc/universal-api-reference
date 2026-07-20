# Create Shared Report with Clockify

Creates a new shared report in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/shared-reports`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Shared Report](https://docs.developer.clockify.me/#tag/Shared-Report/operation/saveSharedReportV1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | — |
| `filter.amounts` | body | `list<string>` | no | Accepted values: `COST`, `EARNED`, `EXPORT`, `HIDE_AMOUNT`, `PROFIT`. Send multiple values as a array. |
| `filter.amountShown` | body | `list` | no | Accepted values: `COST`, `EARNED`, `EXPORT`, `HIDE_AMOUNT`, `PROFIT`. |
| `filter.approvalState` | body | `list` | no | Accepted values: `ALL`, `APPROVED`, `UNAPPROVED`. |
| `filter.archived` | body | `boolean` | no | — |
| `filter.attendanceFilter` | body | `object` | no | — |
| `filter.attendanceFilter.breakFilters[]` | body | `array<object>` | no | — |
| `filter.attendanceFilter.breakFilters[].filtrationType` | body | `list` | no | Accepted values: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `filter.attendanceFilter.breakFilters[].value` | body | `string` | no | — |
| `filter.attendanceFilter.capacityFilters[]` | body | `array<object>` | no | — |
| `filter.attendanceFilter.capacityFilters[].filtrationType` | body | `list` | no | Accepted values: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `filter.attendanceFilter.capacityFilters[].value` | body | `string` | no | — |
| `filter.attendanceFilter.endFilters[]` | body | `array<object>` | no | — |
| `filter.attendanceFilter.endFilters[].filtrationType` | body | `list` | no | Accepted values: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `filter.attendanceFilter.endFilters[].value` | body | `string` | no | — |
| `filter.attendanceFilter.hasTimeOff` | body | `boolean` | no | — |
| `filter.attendanceFilter.overtimeFilters[]` | body | `array<object>` | no | — |
| `filter.attendanceFilter.overtimeFilters[].filtrationType` | body | `list` | no | Accepted values: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `filter.attendanceFilter.overtimeFilters[].value` | body | `string` | no | — |
| `filter.attendanceFilter.page` | body | `number` | no | — |
| `filter.attendanceFilter.pageSize` | body | `number` | no | — |
| `filter.attendanceFilter.sortColumn` | body | `list` | no | Accepted values: `BREAK`, `CAPACITY`, `DATE`, `END`, `OVERTIME`, `START`, `TIME_OFF`, `USER`, `WORK`. |
| `filter.attendanceFilter.startFilters[]` | body | `array<object>` | no | — |
| `filter.attendanceFilter.startFilters[].filtrationType` | body | `list` | no | Accepted values: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `filter.attendanceFilter.startFilters[].value` | body | `string` | no | — |
| `filter.attendanceFilter.workFilters[]` | body | `array<object>` | no | — |
| `filter.attendanceFilter.workFilters[].filtrationType` | body | `list` | no | Accepted values: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `filter.attendanceFilter.workFilters[].value` | body | `string` | no | — |
| `filter.billable` | body | `boolean` | no | — |
| `filter.clients` | body | `object` | no | — |
| `filter.clients.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.clients.ids[]` | body | `array<string>` | no | — |
| `filter.clients.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `filter.currency` | body | `object` | no | — |
| `filter.currency.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.currency.ids[]` | body | `array<string>` | no | — |
| `filter.currency.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `filter.customFields[]` | body | `array<object>` | no | — |
| `filter.customFields[].id` | body | `string` | no | — |
| `filter.customFields[].isEmpty` | body | `boolean` | no | — |
| `filter.customFields[].numberCondition` | body | `list` | no | Accepted values: `EQUAL`, `GREATER_THAN`, `LESS_THAN`. |
| `filter.customFields[].type` | body | `list` | no | Accepted values: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. |
| `filter.customFields[].value` | body | `object` | no | — |
| `filter.dateFormat` | body | `string` | no | — |
| `filter.dateRangeEnd` | body | `string` | yes | — |
| `filter.dateRangeStart` | body | `string` | yes | — |
| `filter.dateRangeType` | body | `list` | no | Accepted values: `ABSOLUTE`, `LAST_MONTH`, `LAST_WEEK`, `LAST_YEAR`, `PAST_TWO_WEEKS`, `THIS_MONTH`, `THIS_WEEK`, `THIS_YEAR`, `TODAY`, `YESTERDAY`. |
| `filter.description` | body | `string` | no | — |
| `filter.detailedFilter` | body | `object` | no | — |
| `filter.detailedFilter.auditFilter` | body | `object` | no | — |
| `filter.detailedFilter.auditFilter.duration` | body | `number` | no | — |
| `filter.detailedFilter.auditFilter.durationShorter` | body | `boolean` | no | — |
| `filter.detailedFilter.auditFilter.withoutProject` | body | `boolean` | no | — |
| `filter.detailedFilter.auditFilter.withoutTask` | body | `boolean` | no | — |
| `filter.detailedFilter.options` | body | `object` | no | — |
| `filter.detailedFilter.options.totals` | body | `list` | no | Accepted values: `CALCULATE`, `EXCLUDE`. |
| `filter.detailedFilter.page` | body | `number` | no | — |
| `filter.detailedFilter.pageSize` | body | `number` | no | — |
| `filter.detailedFilter.sortColumn` | body | `list` | no | Accepted values: `DATE`, `DESCRIPTION`, `DURATION`, `ID`, `NATURAL`, `USER`, `USER_DATE`, `ZONED_DATE`. |
| `filter.exportType` | body | `list` | no | Accepted values: `CSV`, `JSON`, `JSON_V1`, `PDF`, `XLSX`, `ZIP`. |
| `filter.invoicingState` | body | `list` | no | Accepted values: `ALL`, `INVOICED`, `UNINVOICED`. |
| `filter.projects` | body | `object` | no | — |
| `filter.projects.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.projects.ids[]` | body | `array<string>` | no | — |
| `filter.projects.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `filter.rounding` | body | `boolean` | no | — |
| `filter.sortOrder` | body | `list` | no | Accepted values: `ASCENDING`, `DESCENDING`. |
| `filter.summaryFilter` | body | `object` | no | — |
| `filter.summaryFilter.groups[]` | body | `array<string>` | no | — |
| `filter.summaryFilter.sortColumn` | body | `list` | no | Accepted values: `AMOUNT`, `COST`, `DURATION`, `EARNED`, `GROUP`, `PROFIT`. |
| `filter.summaryFilter.summaryChartType` | body | `list` | no | Accepted values: `BILLABILITY`, `PROJECT`. |
| `filter.tags` | body | `object` | no | — |
| `filter.tags.containedInTimeentry` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.tags.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.tags.ids[]` | body | `array<string>` | no | — |
| `filter.tags.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `filter.tasks` | body | `object` | no | — |
| `filter.tasks.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.tasks.ids[]` | body | `array<string>` | no | — |
| `filter.tasks.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `filter.timeFormat` | body | `string` | no | — |
| `filter.timeZone` | body | `string` | no | — |
| `filter.userCustomFields[]` | body | `array<object>` | no | — |
| `filter.userCustomFields[].id` | body | `string` | no | — |
| `filter.userCustomFields[].isEmpty` | body | `boolean` | no | — |
| `filter.userCustomFields[].numberCondition` | body | `list` | no | Accepted values: `EQUAL`, `GREATER_THAN`, `LESS_THAN`. |
| `filter.userCustomFields[].type` | body | `list` | no | Accepted values: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. |
| `filter.userCustomFields[].value` | body | `object` | no | — |
| `filter.userGroups` | body | `object` | no | — |
| `filter.userGroups.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.userGroups.ids[]` | body | `array<string>` | no | — |
| `filter.userGroups.status` | body | `list` | no | Accepted values: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `filter.userLocale` | body | `string` | no | — |
| `filter.users` | body | `object` | no | — |
| `filter.users.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.users.ids[]` | body | `array<string>` | no | — |
| `filter.users.status` | body | `list` | no | Accepted values: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `filter.weeklyFilter` | body | `object` | no | — |
| `filter.weeklyFilter.group` | body | `string` | no | — |
| `filter.weeklyFilter.subgroup` | body | `string` | no | — |
| `filter.weekStart` | body | `list` | no | Accepted values: `FRIDAY`, `MONDAY`, `SATURDAY`, `SUNDAY`, `THURSDAY`, `TUESDAY`, `WEDNESDAY`. |
| `filter.withoutDescription` | body | `boolean` | no | — |
| `filter.zoomLevel` | body | `list` | no | Accepted values: `MONTH`, `WEEK`, `YEAR`. |
| `fixedDate` | body | `boolean` | no | — |
| `isPublic` | body | `boolean` | no | — |
| `name` | body | `string` | no | — |
| `type` | body | `list` | no | Accepted values: `ATTENDANCE`, `DETAILED`, `EXPENSE_DETAILED`, `EXPENSE_RECEIPT`, `INVOICES`, `INVOICE_EXPENSE`, `INVOICE_TIME`, `KIOSK_ASSIGNEES`, `KIOSK_PIN_LIST`, `PROJECT`, `PTO_BALANCE`, `PTO_REQUESTS`, `SCHEDULED`, `SUMMARY`, `TEAM_FULL`, `TEAM_GROUPS`, `TEAM_LIMITED`, `WEEKLY`. |
| `visibleToUserGroups[]` | body | `array<string>` | no | — |
| `visibleToUsers[]` | body | `array<string>` | no | — |
| `workspaceId` | path | `list<string>` | yes | — |
