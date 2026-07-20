# Clockify: Generate Detailed Report

Generates a detailed report in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-detailed-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-detailed-report?connectionId=$CONNECTION_ID&workspaceId=string&dateRangeStart=2026-02-01&dateRangeEnd=2026-02-23&detailedFilter=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "dateRangeStart": "2026-02-01",
  "dateRangeEnd": "2026-02-23",
  "detailedFilter": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-detailed-report?${params}`, {
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
| `amountShown` | list<string> | no | One of: `COST`, `EARNED`, `EXPORT`, `HIDE_AMOUNT`, `PROFIT`. |
| `approvalState` | list<string> | no | One of: `ALL`, `APPROVED`, `UNAPPROVED`. |
| `archived` | boolean | no |  |
| `attendanceFilter` | object | no |  |
| `attendanceFilter.breakFilters[]` | array<object> | no |  |
| `attendanceFilter.breakFilters[].filtrationType` | list<string> | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.breakFilters[].value` | string | no |  |
| `attendanceFilter.capacityFilters[]` | array<object> | no |  |
| `attendanceFilter.capacityFilters[].filtrationType` | list<string> | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.capacityFilters[].value` | string | no |  |
| `attendanceFilter.endFilters[]` | array<object> | no |  |
| `attendanceFilter.endFilters[].filtrationType` | list<string> | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.endFilters[].value` | string | no |  |
| `attendanceFilter.hasTimeOff` | boolean | no |  |
| `attendanceFilter.overtimeFilters[]` | array<object> | no |  |
| `attendanceFilter.overtimeFilters[].filtrationType` | list<string> | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.overtimeFilters[].value` | string | no |  |
| `attendanceFilter.page` | number | no |  |
| `attendanceFilter.pageSize` | number | no |  |
| `attendanceFilter.sortColumn` | list<string> | no | One of: `BREAK`, `CAPACITY`, `DATE`, `END`, `OVERTIME`, `START`, `TIME_OFF`, `USER`, `WORK`. |
| `attendanceFilter.startFilters[]` | array<object> | no |  |
| `attendanceFilter.startFilters[].filtrationType` | list<string> | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.startFilters[].value` | string | no |  |
| `attendanceFilter.workFilters[]` | array<object> | no |  |
| `attendanceFilter.workFilters[].filtrationType` | list<string> | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `attendanceFilter.workFilters[].value` | string | no |  |
| `billable` | boolean | no |  |
| `clients` | object | no |  |
| `clients.contains` | list<string> | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `clients.ids[]` | array<string> | no |  |
| `clients.status` | list<string> | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `currency` | object | no |  |
| `currency.contains` | list<string> | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `currency.ids[]` | array<string> | no |  |
| `currency.status` | list<string> | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `customFields[]` | array<object> | no |  |
| `customFields[].id` | string | no |  |
| `customFields[].isEmpty` | boolean | no |  |
| `customFields[].numberCondition` | list<string> | no | One of: `EQUAL`, `GREATER_THAN`, `LESS_THAN`. |
| `customFields[].type` | list<string> | no | One of: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. |
| `customFields[].value` | object | no |  |
| `dateFormat` | string | no |  |
| `dateRangeType` | list<string> | no | One of: `ABSOLUTE`, `LAST_MONTH`, `LAST_WEEK`, `LAST_YEAR`, `PAST_TWO_WEEKS`, `THIS_MONTH`, `THIS_WEEK`, `THIS_YEAR`, `TODAY`, `YESTERDAY`. |
| `description` | string | no |  |
| `detailedFilter.auditFilter` | object | no |  |
| `detailedFilter.auditFilter.duration` | number | no |  |
| `detailedFilter.auditFilter.durationShorter` | boolean | no |  |
| `detailedFilter.auditFilter.withoutProject` | boolean | no |  |
| `detailedFilter.auditFilter.withoutTask` | boolean | no |  |
| `detailedFilter.options` | object | no |  |
| `detailedFilter.options.totals` | list<string> | no | One of: `CALCULATE`, `EXCLUDE`. |
| `exportType` | list<string> | no | One of: `CSV`, `JSON`, `JSON_V1`, `PDF`, `XLSX`, `ZIP`. |
| `invoicingState` | list<string> | no | One of: `ALL`, `INVOICED`, `UNINVOICED`. |
| `projects` | object | no |  |
| `projects.contains` | list<string> | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `projects.ids[]` | array<string> | no |  |
| `projects.status` | list<string> | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `rounding` | boolean | no |  |
| `sortOrder` | list<string> | no | One of: `ASCENDING`, `DESCENDING`. |
| `summaryFilter` | object | no |  |
| `summaryFilter.groups[]` | array<string> | no |  |
| `summaryFilter.sortColumn` | list<string> | no | One of: `AMOUNT`, `COST`, `DURATION`, `EARNED`, `GROUP`, `PROFIT`. |
| `summaryFilter.summaryChartType` | list<string> | no | One of: `BILLABILITY`, `PROJECT`. |
| `tags` | object | no |  |
| `tags.containedInTimeentry` | list<string> | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `tags.contains` | list<string> | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `tags.ids[]` | array<string> | no |  |
| `tags.status` | list<string> | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `tasks` | object | no |  |
| `tasks.contains` | list<string> | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `tasks.ids[]` | array<string> | no |  |
| `tasks.status` | list<string> | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `timeFormat` | string | no |  |
| `timeZone` | string | no |  |
| `userCustomFields[]` | array<object> | no |  |
| `userCustomFields[].id` | string | no |  |
| `userCustomFields[].isEmpty` | boolean | no |  |
| `userCustomFields[].numberCondition` | list<string> | no | One of: `EQUAL`, `GREATER_THAN`, `LESS_THAN`. |
| `userCustomFields[].type` | list<string> | no | One of: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. |
| `userCustomFields[].value` | object | no |  |
| `userGroups` | object | no |  |
| `userGroups.contains` | list<string> | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userGroups.ids[]` | array<string> | no |  |
| `userGroups.status` | list<string> | no | One of: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `userLocale` | string | no |  |
| `users` | object | no |  |
| `users.contains` | list<string> | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `users.ids[]` | array<string> | no |  |
| `users.status` | list<string> | no | One of: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `weeklyFilter` | object | no |  |
| `weeklyFilter.group` | string | no |  |
| `weeklyFilter.subgroup` | string | no |  |
| `weekStart` | list<string> | no | One of: `FRIDAY`, `MONDAY`, `SATURDAY`, `SUNDAY`, `THURSDAY`, `TUESDAY`, `WEDNESDAY`. |
| `withoutDescription` | boolean | no |  |
| `workspaceId` | list<string> | yes |  |
| `zoomLevel` | list<string> | no | One of: `MONTH`, `WEEK`, `YEAR`. |
| `dateRangeStart` | string | yes | Example: `2026-02-01`. |
| `dateRangeEnd` | string | yes | Example: `2026-02-23`. |
| `detailedFilter` | object | yes |  |
| `detailedFilter.page` | number | no | Default: `1`. Example: `1`. |
| `detailedFilter.pageSize` | number | no | Example: `50`. |
| `detailedFilter.sortColumn` | list<string> | no | One of: `DATE`, `DESCRIPTION`, `DURATION`, `ID`, `NATURAL`, `USER`, `USER_DATE`, `ZONED_DATE`. Example: `DATE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "timeentries": [
        {
          "amount": 1,
          "approvalRequestId": "string",
          "billable": true,
          "clientId": "string",
          "clientName": "Ava Chen",
          "costAmount": 1,
          "costRate": 1,
          "currency": "string",
          "description": "string",
          "earnedAmount": 1,
          "earnedRate": 1,
          "id": "string",
          "isLocked": true,
          "locked": true,
          "projectColor": "string",
          "projectId": "string",
          "projectName": "Ava Chen",
          "rate": 1,
          "tagIds": [
            "string"
          ],
          "tags": [
            {
              "id": "string",
              "name": "Ava Chen"
            }
          ],
          "taskId": "string",
          "taskName": "Ava Chen",
          "timeInterval": {
            "duration": 1,
            "end": "2026-05-07T12:00:00.000Z",
            "offEnd": 1,
            "offStart": 1,
            "start": "2026-05-07T12:00:00.000Z",
            "timeZone": "string",
            "zonedEnd": "2026-05-07T12:00:00.000Z",
            "zonedStart": "2026-05-07T12:00:00.000Z"
          },
          "type": "string",
          "userEmail": "ava@example.com",
          "userId": "string",
          "userName": "Ava Chen"
        }
      ],
      "totals": [
        {
          "amounts": [
            {
              "amountByCurrency": [
                {
                  "amount": 1,
                  "currency": "string"
                }
              ],
              "type": "string",
              "value": 1
            }
          ],
          "entriesCount": 1,
          "id": "string",
          "numOfCurrencies": 1,
          "totalAmount": 1,
          "totalAmountByCurrency": [
            {
              "amount": 1,
              "currency": "string"
            }
          ],
          "totalBillableTime": 1,
          "totalTime": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `timeentries` | array<object> |  |
| `timeentries[].amount` | number |  |
| `timeentries[].approvalRequestId` | string |  |
| `timeentries[].billable` | boolean |  |
| `timeentries[].clientId` | string |  |
| `timeentries[].clientName` | string |  |
| `timeentries[].costAmount` | number |  |
| `timeentries[].costRate` | number |  |
| `timeentries[].currency` | string |  |
| `timeentries[].description` | string |  |
| `timeentries[].earnedAmount` | number |  |
| `timeentries[].earnedRate` | number |  |
| `timeentries[].id` | string |  |
| `timeentries[].isLocked` | boolean |  |
| `timeentries[].locked` | boolean |  |
| `timeentries[].projectColor` | string |  |
| `timeentries[].projectId` | string |  |
| `timeentries[].projectName` | string |  |
| `timeentries[].rate` | number |  |
| `timeentries[].tagIds` | array<string> |  |
| `timeentries[].tags` | array<object> |  |
| `timeentries[].tags[].id` | string |  |
| `timeentries[].tags[].name` | string |  |
| `timeentries[].taskId` | string |  |
| `timeentries[].taskName` | string |  |
| `timeentries[].timeInterval` | object |  |
| `timeentries[].timeInterval.duration` | number |  |
| `timeentries[].timeInterval.end` | date |  |
| `timeentries[].timeInterval.offEnd` | number |  |
| `timeentries[].timeInterval.offStart` | number |  |
| `timeentries[].timeInterval.start` | date |  |
| `timeentries[].timeInterval.timeZone` | string |  |
| `timeentries[].timeInterval.zonedEnd` | date |  |
| `timeentries[].timeInterval.zonedStart` | date |  |
| `timeentries[].type` | string |  |
| `timeentries[].userEmail` | string |  |
| `timeentries[].userId` | string |  |
| `timeentries[].userName` | string |  |
| `totals` | array<object> |  |
| `totals[].amounts` | array<object> |  |
| `totals[].amounts[].amountByCurrency` | array<object> |  |
| `totals[].amounts[].amountByCurrency[].amount` | number |  |
| `totals[].amounts[].amountByCurrency[].currency` | string |  |
| `totals[].amounts[].type` | string |  |
| `totals[].amounts[].value` | number |  |
| `totals[].entriesCount` | number |  |
| `totals[].id` | string |  |
| `totals[].numOfCurrencies` | number |  |
| `totals[].totalAmount` | number |  |
| `totals[].totalAmountByCurrency` | array<object> |  |
| `totals[].totalAmountByCurrency[].amount` | number |  |
| `totals[].totalAmountByCurrency[].currency` | string |  |
| `totals[].totalBillableTime` | number |  |
| `totals[].totalTime` | number |  |

## Native endpoint

Through the native Clockify API, this operation is `POST https://reports.api.clockify.me/v1/workspaces/:workspaceId/reports/detailed` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-detailed-report.md) for the provider-specific parameters and requirements.

