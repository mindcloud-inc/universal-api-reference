# Clockify: Generate Summary Report

Generates a summary report in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-summary-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-summary-report?connectionId=$CONNECTION_ID&workspaceId=string&dateRangeStart=2026-02-01T00%3A00%3A00.000Z&dateRangeEnd=2026-02-23T23%3A59%3A59.999Z&summaryFilter=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "dateRangeStart": "2026-02-01T00:00:00.000Z",
  "dateRangeEnd": "2026-02-23T23:59:59.999Z",
  "summaryFilter": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-summary-report?${params}`, {
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
| `detailedFilter` | object | no |  |
| `detailedFilter.auditFilter` | object | no |  |
| `detailedFilter.auditFilter.duration` | number | no |  |
| `detailedFilter.auditFilter.durationShorter` | boolean | no |  |
| `detailedFilter.auditFilter.withoutProject` | boolean | no |  |
| `detailedFilter.auditFilter.withoutTask` | boolean | no |  |
| `detailedFilter.options` | object | no |  |
| `detailedFilter.options.totals` | list<string> | no | One of: `CALCULATE`, `EXCLUDE`. |
| `detailedFilter.page` | number | no |  |
| `detailedFilter.pageSize` | number | no |  |
| `detailedFilter.sortColumn` | list<string> | no | One of: `DATE`, `DESCRIPTION`, `DURATION`, `ID`, `NATURAL`, `USER`, `USER_DATE`, `ZONED_DATE`. |
| `exportType` | list<string> | no | One of: `CSV`, `JSON`, `JSON_V1`, `PDF`, `XLSX`, `ZIP`. |
| `invoicingState` | list<string> | no | One of: `ALL`, `INVOICED`, `UNINVOICED`. |
| `projects` | object | no |  |
| `projects.contains` | list<string> | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `projects.ids[]` | array<string> | no |  |
| `projects.status` | list<string> | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `rounding` | boolean | no |  |
| `sortOrder` | list<string> | no | One of: `ASCENDING`, `DESCENDING`. |
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
| `dateRangeStart` | string | yes | Example: `2026-02-01T00:00:00.000Z`. |
| `dateRangeEnd` | string | yes | Example: `2026-02-23T23:59:59.999Z`. |
| `summaryFilter` | object | yes |  |
| `summaryFilter.groups[]` | array<string> | no | Example: `PROJECT`. |
| `summaryFilter.sortColumn` | list<string> | no | One of: `AMOUNT`, `COST`, `DURATION`, `EARNED`, `GROUP`, `PROFIT`. Example: `GROUP`. |
| `summaryFilter.summaryChartType` | list<string> | no | One of: `BILLABILITY`, `PROJECT`. Example: `PROJECT`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "donutChart": [
        {
          "earned": 1,
          "id": "string",
          "totalAmount": 1,
          "totalBillableTime": 1,
          "totalTime": 1
        }
      ],
      "groupOne": [
        {
          "amount": 1,
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
          "children": [
            {
              "amount": 1,
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
              "children": [
                {}
              ],
              "clientName": "Ava Chen",
              "color": "string",
              "currency": "string",
              "days": [
                {
                  "amount": 1,
                  "date": "2026-05-07T12:00:00.000Z",
                  "duration": 1
                }
              ],
              "duration": 1,
              "id": "string",
              "name": "Ava Chen",
              "nameLowerCase": "Ava Chen",
              "workspaceCurrencyCode": "string"
            }
          ],
          "clientName": "Ava Chen",
          "color": "string",
          "currency": "string",
          "days": [
            {
              "amount": 1,
              "date": "2026-05-07T12:00:00.000Z",
              "duration": 1
            }
          ],
          "duration": 1,
          "id": "string",
          "name": "Ava Chen",
          "nameLowerCase": "Ava Chen",
          "workspaceCurrencyCode": "string"
        }
      ],
      "groupTotals": {
        "groupOneTotalCount": 1
      },
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
| `donutChart` | array<object> |  |
| `donutChart[].earned` | number |  |
| `donutChart[].id` | string |  |
| `donutChart[].totalAmount` | number |  |
| `donutChart[].totalBillableTime` | number |  |
| `donutChart[].totalTime` | number |  |
| `groupOne` | array<object> |  |
| `groupOne[].amount` | number |  |
| `groupOne[].amounts` | array<object> |  |
| `groupOne[].amounts[].amountByCurrency` | array<object> |  |
| `groupOne[].amounts[].amountByCurrency[].amount` | number |  |
| `groupOne[].amounts[].amountByCurrency[].currency` | string |  |
| `groupOne[].amounts[].type` | string |  |
| `groupOne[].amounts[].value` | number |  |
| `groupOne[].children` | array<object> |  |
| `groupOne[].children[].amount` | number |  |
| `groupOne[].children[].amounts` | array<object> |  |
| `groupOne[].children[].amounts[].amountByCurrency` | array<object> |  |
| `groupOne[].children[].amounts[].amountByCurrency[].amount` | number |  |
| `groupOne[].children[].amounts[].amountByCurrency[].currency` | string |  |
| `groupOne[].children[].amounts[].type` | string |  |
| `groupOne[].children[].amounts[].value` | number |  |
| `groupOne[].children[].children` | array<object> |  |
| `groupOne[].children[].clientName` | string |  |
| `groupOne[].children[].color` | string |  |
| `groupOne[].children[].currency` | string |  |
| `groupOne[].children[].days` | array<object> |  |
| `groupOne[].children[].days[].amount` | number |  |
| `groupOne[].children[].days[].date` | date |  |
| `groupOne[].children[].days[].duration` | number |  |
| `groupOne[].children[].duration` | number |  |
| `groupOne[].children[].id` | string |  |
| `groupOne[].children[].name` | string |  |
| `groupOne[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].workspaceCurrencyCode` | string |  |
| `groupOne[].clientName` | string |  |
| `groupOne[].color` | string |  |
| `groupOne[].currency` | string |  |
| `groupOne[].days` | array<object> |  |
| `groupOne[].days[].amount` | number |  |
| `groupOne[].days[].date` | date |  |
| `groupOne[].days[].duration` | number |  |
| `groupOne[].duration` | number |  |
| `groupOne[].id` | string |  |
| `groupOne[].name` | string |  |
| `groupOne[].nameLowerCase` | string |  |
| `groupOne[].workspaceCurrencyCode` | string |  |
| `groupTotals` | object |  |
| `groupTotals.groupOneTotalCount` | number |  |
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

Through the native Clockify API, this operation is `POST https://reports.api.clockify.me/v1/workspaces/:workspaceId/reports/summary` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-summary-report.md) for the provider-specific parameters and requirements.

