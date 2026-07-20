# Clockify: Generate Weekly Report

Generates a weekly report in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-weekly-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-weekly-report?connectionId=$CONNECTION_ID&dateRangeEnd=string&dateRangeStart=string&weeklyFilter=%5Bobject%20Object%5D&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateRangeEnd": "string",
  "dateRangeStart": "string",
  "weeklyFilter": "[object Object]",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-weekly-report?${params}`, {
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
| `amounts` | list<string> | no | One of: `COST`, `EARNED`, `EXPORT`, `HIDE_AMOUNT`, `PROFIT`. Accepts multiple values as an array. |
| `amountShown` | list | no | One of: `COST`, `EARNED`, `EXPORT`, `HIDE_AMOUNT`, `PROFIT`. |
| `approvalState` | list | no | One of: `ALL`, `APPROVED`, `UNAPPROVED`. |
| `archived` | boolean | no |  |
| `attendanceFilter` | object | no |  |
| `attendanceFilter.breakFilters[]` | array<object> | no |  |
| `attendanceFilter.breakFilters[].filtrationType` | list | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.breakFilters[].value` | string | no |  |
| `attendanceFilter.capacityFilters[]` | array<object> | no |  |
| `attendanceFilter.capacityFilters[].filtrationType` | list | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.capacityFilters[].value` | string | no |  |
| `attendanceFilter.endFilters[]` | array<object> | no |  |
| `attendanceFilter.endFilters[].filtrationType` | list | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.endFilters[].value` | string | no |  |
| `attendanceFilter.hasTimeOff` | boolean | no |  |
| `attendanceFilter.overtimeFilters[]` | array<object> | no |  |
| `attendanceFilter.overtimeFilters[].filtrationType` | list | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.overtimeFilters[].value` | string | no |  |
| `attendanceFilter.page` | number | no |  |
| `attendanceFilter.pageSize` | number | no |  |
| `attendanceFilter.sortColumn` | list | no | One of: `BREAK`, `CAPACITY`, `DATE`, `END`, `OVERTIME`, `START`, `TIME_OFF`, `USER`, `WORK`. |
| `attendanceFilter.startFilters[]` | array<object> | no |  |
| `attendanceFilter.startFilters[].filtrationType` | list | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.startFilters[].value` | string | no |  |
| `attendanceFilter.workFilters[]` | array<object> | no |  |
| `attendanceFilter.workFilters[].filtrationType` | list | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.workFilters[].value` | string | no |  |
| `billable` | boolean | no |  |
| `clients` | object | no |  |
| `clients.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `clients.ids[]` | array<string> | no |  |
| `clients.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `currency` | object | no |  |
| `currency.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `currency.ids[]` | array<string> | no |  |
| `currency.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `customFields[]` | array<object> | no |  |
| `customFields[].id` | string | no |  |
| `customFields[].isEmpty` | boolean | no |  |
| `customFields[].numberCondition` | list | no | One of: `EQUAL`, `GREATER_THAN`, `LESS_THAN`. |
| `customFields[].type` | list | no | One of: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. |
| `customFields[].value` | object | no |  |
| `dateFormat` | string | no |  |
| `dateRangeEnd` | string | yes |  |
| `dateRangeStart` | string | yes |  |
| `dateRangeType` | list | no | One of: `ABSOLUTE`, `LAST_MONTH`, `LAST_WEEK`, `LAST_YEAR`, `PAST_TWO_WEEKS`, `THIS_MONTH`, `THIS_WEEK`, `THIS_YEAR`, `TODAY`, `YESTERDAY`. |
| `description` | string | no |  |
| `detailedFilter` | object | no |  |
| `detailedFilter.auditFilter` | object | no |  |
| `detailedFilter.auditFilter.duration` | number | no |  |
| `detailedFilter.auditFilter.durationShorter` | boolean | no |  |
| `detailedFilter.auditFilter.withoutProject` | boolean | no |  |
| `detailedFilter.auditFilter.withoutTask` | boolean | no |  |
| `detailedFilter.options` | object | no |  |
| `detailedFilter.options.totals` | list | no | One of: `CALCULATE`, `EXCLUDE`. |
| `detailedFilter.page` | number | no |  |
| `detailedFilter.pageSize` | number | no |  |
| `detailedFilter.sortColumn` | list | no | One of: `DATE`, `DESCRIPTION`, `DURATION`, `ID`, `NATURAL`, `USER`, `USER_DATE`, `ZONED_DATE`. |
| `exportType` | list | no | One of: `CSV`, `JSON`, `JSON_V1`, `PDF`, `XLSX`, `ZIP`. |
| `invoicingState` | list | no | One of: `ALL`, `INVOICED`, `UNINVOICED`. |
| `projects` | object | no |  |
| `projects.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `projects.ids[]` | array<string> | no |  |
| `projects.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `rounding` | boolean | no |  |
| `sortOrder` | list | no | One of: `ASCENDING`, `DESCENDING`. |
| `summaryFilter` | object | no |  |
| `summaryFilter.groups[]` | array<string> | no |  |
| `summaryFilter.sortColumn` | list | no | One of: `AMOUNT`, `COST`, `DURATION`, `EARNED`, `GROUP`, `PROFIT`. |
| `summaryFilter.summaryChartType` | list | no | One of: `BILLABILITY`, `PROJECT`. |
| `tags` | object | no |  |
| `tags.containedInTimeentry` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `tags.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `tags.ids[]` | array<string> | no |  |
| `tags.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `tasks` | object | no |  |
| `tasks.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `tasks.ids[]` | array<string> | no |  |
| `tasks.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `timeFormat` | string | no |  |
| `timeZone` | string | no |  |
| `userCustomFields[]` | array<object> | no |  |
| `userCustomFields[].id` | string | no |  |
| `userCustomFields[].isEmpty` | boolean | no |  |
| `userCustomFields[].numberCondition` | list | no | One of: `EQUAL`, `GREATER_THAN`, `LESS_THAN`. |
| `userCustomFields[].type` | list | no | One of: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. |
| `userCustomFields[].value` | object | no |  |
| `userGroups` | object | no |  |
| `userGroups.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userGroups.ids[]` | array<string> | no |  |
| `userGroups.status` | list | no | One of: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `userLocale` | string | no |  |
| `users` | object | no |  |
| `users.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `users.ids[]` | array<string> | no |  |
| `users.status` | list | no | One of: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `weeklyFilter` | object | yes |  |
| `weeklyFilter.group` | string | no |  |
| `weeklyFilter.subgroup` | string | no |  |
| `weekStart` | list | no | One of: `FRIDAY`, `MONDAY`, `SATURDAY`, `SUNDAY`, `THURSDAY`, `TUESDAY`, `WEDNESDAY`. |
| `withoutDescription` | boolean | no |  |
| `workspaceId` | list<string> | yes |  |
| `zoomLevel` | list | no | One of: `MONTH`, `WEEK`, `YEAR`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "decimalFormat": true,
      "groupOne": [
        [
          {}
        ]
      ],
      "includeUsersWithoutTime": true,
      "totals": [
        [
          {}
        ]
      ],
      "totalsByDay": [
        [
          {}
        ]
      ],
      "trackTimeDownToSeconds": true,
      "usersWithoutTime": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `decimalFormat` | boolean |  |
| `groupOne[]` | array<object> |  |
| `groupOne[].amount` | number |  |
| `groupOne[].children[]` | array<object> |  |
| `groupOne[].children[].amount` | number |  |
| `groupOne[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].clientName` | string |  |
| `groupOne[].children[].days[]` | array<object> |  |
| `groupOne[].children[].days[].amount` | number |  |
| `groupOne[].children[].days[].date` | string |  |
| `groupOne[].children[].days[].duration` | number |  |
| `groupOne[].children[].duration` | number |  |
| `groupOne[].children[].id` | string |  |
| `groupOne[].children[].name` | string |  |
| `groupOne[].children[].nameLowerCase` | string |  |
| `groupOne[].clientName` | string |  |
| `groupOne[].days[]` | array<object> |  |
| `groupOne[].days[].amount` | number |  |
| `groupOne[].days[].date` | string |  |
| `groupOne[].days[].duration` | number |  |
| `groupOne[].duration` | number |  |
| `groupOne[].id` | string |  |
| `groupOne[].name` | string |  |
| `groupOne[].nameLowerCase` | string |  |
| `includeUsersWithoutTime` | boolean |  |
| `totals[]` | array<object> |  |
| `totals[].amounts[]` | array<object> |  |
| `totals[].amounts[].type` | string |  |
| `totals[].amounts[].value` | number |  |
| `totals[].entriesCount` | number |  |
| `totals[].id` | string |  |
| `totals[].totalBillableTime` | number |  |
| `totals[].totalTime` | number |  |
| `totalsByDay[]` | array<object> |  |
| `totalsByDay[].amount` | number |  |
| `totalsByDay[].date` | string |  |
| `totalsByDay[].duration` | number |  |
| `trackTimeDownToSeconds` | boolean |  |
| `usersWithoutTime[]` | array<object> |  |
| `usersWithoutTime[].dateFormat` | string |  |
| `usersWithoutTime[].email` | string |  |
| `usersWithoutTime[].id` | string |  |
| `usersWithoutTime[].name` | string |  |
| `usersWithoutTime[].timeFormat` | string |  |
| `usersWithoutTime[].timeZone` | string |  |
| `usersWithoutTime[].weekStart` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST https://reports.api.clockify.me/v1/workspaces/:workspaceId/reports/weekly` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-weekly-report.md) for the provider-specific parameters and requirements.

