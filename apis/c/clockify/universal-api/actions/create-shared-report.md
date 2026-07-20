# Clockify: Create Shared Report

Creates a new shared report in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-shared-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-shared-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filter.dateRangeEnd": "string",
  "filter.dateRangeStart": "string",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-shared-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filter.dateRangeEnd": "string",
    "filter.dateRangeStart": "string",
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | object | no |  |
| `filter.amounts` | list<string> | no | One of: `COST`, `EARNED`, `EXPORT`, `HIDE_AMOUNT`, `PROFIT`. Accepts multiple values as an array. |
| `filter.amountShown` | list | no | One of: `COST`, `EARNED`, `EXPORT`, `HIDE_AMOUNT`, `PROFIT`. |
| `filter.approvalState` | list | no | One of: `ALL`, `APPROVED`, `UNAPPROVED`. |
| `filter.archived` | boolean | no |  |
| `filter.attendanceFilter` | object | no |  |
| `filter.attendanceFilter.breakFilters[]` | array<object> | no |  |
| `filter.attendanceFilter.breakFilters[].filtrationType` | list | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `filter.attendanceFilter.breakFilters[].value` | string | no |  |
| `filter.attendanceFilter.capacityFilters[]` | array<object> | no |  |
| `filter.attendanceFilter.capacityFilters[].filtrationType` | list | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `filter.attendanceFilter.capacityFilters[].value` | string | no |  |
| `filter.attendanceFilter.endFilters[]` | array<object> | no |  |
| `filter.attendanceFilter.endFilters[].filtrationType` | list | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `filter.attendanceFilter.endFilters[].value` | string | no |  |
| `filter.attendanceFilter.hasTimeOff` | boolean | no |  |
| `filter.attendanceFilter.overtimeFilters[]` | array<object> | no |  |
| `filter.attendanceFilter.overtimeFilters[].filtrationType` | list | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `filter.attendanceFilter.overtimeFilters[].value` | string | no |  |
| `filter.attendanceFilter.page` | number | no |  |
| `filter.attendanceFilter.pageSize` | number | no |  |
| `filter.attendanceFilter.sortColumn` | list | no | One of: `BREAK`, `CAPACITY`, `DATE`, `END`, `OVERTIME`, `START`, `TIME_OFF`, `USER`, `WORK`. |
| `filter.attendanceFilter.startFilters[]` | array<object> | no |  |
| `filter.attendanceFilter.startFilters[].filtrationType` | list | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `filter.attendanceFilter.startFilters[].value` | string | no |  |
| `filter.attendanceFilter.workFilters[]` | array<object> | no |  |
| `filter.attendanceFilter.workFilters[].filtrationType` | list | no | One of: `EXACTLY`, `LARGER_THAN`, `SMALLER_THAN`. |
| `filter.attendanceFilter.workFilters[].value` | string | no |  |
| `filter.billable` | boolean | no |  |
| `filter.clients` | object | no |  |
| `filter.clients.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.clients.ids[]` | array<string> | no |  |
| `filter.clients.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `filter.currency` | object | no |  |
| `filter.currency.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.currency.ids[]` | array<string> | no |  |
| `filter.currency.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `filter.customFields[]` | array<object> | no |  |
| `filter.customFields[].id` | string | no |  |
| `filter.customFields[].isEmpty` | boolean | no |  |
| `filter.customFields[].numberCondition` | list | no | One of: `EQUAL`, `GREATER_THAN`, `LESS_THAN`. |
| `filter.customFields[].type` | list | no | One of: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. |
| `filter.customFields[].value` | object | no |  |
| `filter.dateFormat` | string | no |  |
| `filter.dateRangeEnd` | string | yes |  |
| `filter.dateRangeStart` | string | yes |  |
| `filter.dateRangeType` | list | no | One of: `ABSOLUTE`, `LAST_MONTH`, `LAST_WEEK`, `LAST_YEAR`, `PAST_TWO_WEEKS`, `THIS_MONTH`, `THIS_WEEK`, `THIS_YEAR`, `TODAY`, `YESTERDAY`. |
| `filter.description` | string | no |  |
| `filter.detailedFilter` | object | no |  |
| `filter.detailedFilter.auditFilter` | object | no |  |
| `filter.detailedFilter.auditFilter.duration` | number | no |  |
| `filter.detailedFilter.auditFilter.durationShorter` | boolean | no |  |
| `filter.detailedFilter.auditFilter.withoutProject` | boolean | no |  |
| `filter.detailedFilter.auditFilter.withoutTask` | boolean | no |  |
| `filter.detailedFilter.options` | object | no |  |
| `filter.detailedFilter.options.totals` | list | no | One of: `CALCULATE`, `EXCLUDE`. |
| `filter.detailedFilter.page` | number | no |  |
| `filter.detailedFilter.pageSize` | number | no |  |
| `filter.detailedFilter.sortColumn` | list | no | One of: `DATE`, `DESCRIPTION`, `DURATION`, `ID`, `NATURAL`, `USER`, `USER_DATE`, `ZONED_DATE`. |
| `filter.exportType` | list | no | One of: `CSV`, `JSON`, `JSON_V1`, `PDF`, `XLSX`, `ZIP`. |
| `filter.invoicingState` | list | no | One of: `ALL`, `INVOICED`, `UNINVOICED`. |
| `filter.projects` | object | no |  |
| `filter.projects.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.projects.ids[]` | array<string> | no |  |
| `filter.projects.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `filter.rounding` | boolean | no |  |
| `filter.sortOrder` | list | no | One of: `ASCENDING`, `DESCENDING`. |
| `filter.summaryFilter` | object | no |  |
| `filter.summaryFilter.groups[]` | array<string> | no |  |
| `filter.summaryFilter.sortColumn` | list | no | One of: `AMOUNT`, `COST`, `DURATION`, `EARNED`, `GROUP`, `PROFIT`. |
| `filter.summaryFilter.summaryChartType` | list | no | One of: `BILLABILITY`, `PROJECT`. |
| `filter.tags` | object | no |  |
| `filter.tags.containedInTimeentry` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.tags.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.tags.ids[]` | array<string> | no |  |
| `filter.tags.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `filter.tasks` | object | no |  |
| `filter.tasks.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.tasks.ids[]` | array<string> | no |  |
| `filter.tasks.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `filter.timeFormat` | string | no |  |
| `filter.timeZone` | string | no |  |
| `filter.userCustomFields[]` | array<object> | no |  |
| `filter.userCustomFields[].id` | string | no |  |
| `filter.userCustomFields[].isEmpty` | boolean | no |  |
| `filter.userCustomFields[].numberCondition` | list | no | One of: `EQUAL`, `GREATER_THAN`, `LESS_THAN`. |
| `filter.userCustomFields[].type` | list | no | One of: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. |
| `filter.userCustomFields[].value` | object | no |  |
| `filter.userGroups` | object | no |  |
| `filter.userGroups.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.userGroups.ids[]` | array<string> | no |  |
| `filter.userGroups.status` | list | no | One of: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `filter.userLocale` | string | no |  |
| `filter.users` | object | no |  |
| `filter.users.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `filter.users.ids[]` | array<string> | no |  |
| `filter.users.status` | list | no | One of: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `filter.weeklyFilter` | object | no |  |
| `filter.weeklyFilter.group` | string | no |  |
| `filter.weeklyFilter.subgroup` | string | no |  |
| `filter.weekStart` | list | no | One of: `FRIDAY`, `MONDAY`, `SATURDAY`, `SUNDAY`, `THURSDAY`, `TUESDAY`, `WEDNESDAY`. |
| `filter.withoutDescription` | boolean | no |  |
| `filter.zoomLevel` | list | no | One of: `MONTH`, `WEEK`, `YEAR`. |
| `fixedDate` | boolean | no |  |
| `isPublic` | boolean | no |  |
| `name` | string | no |  |
| `type` | list | no | One of: `ATTENDANCE`, `DETAILED`, `EXPENSE_DETAILED`, `EXPENSE_RECEIPT`, `INVOICES`, `INVOICE_EXPENSE`, `INVOICE_TIME`, `KIOSK_ASSIGNEES`, `KIOSK_PIN_LIST`, `PROJECT`, `PTO_BALANCE`, `PTO_REQUESTS`, `SCHEDULED`, `SUMMARY`, `TEAM_FULL`, `TEAM_GROUPS`, `TEAM_LIMITED`, `WEEKLY`. |
| `visibleToUserGroups[]` | array<string> | no |  |
| `visibleToUsers[]` | array<string> | no |  |
| `workspaceId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filter": {
        "amounts": [
          [
            "string"
          ]
        ],
        "amountShown": "string",
        "approvalState": "string",
        "archived": true,
        "attendanceFilter": {
          "breakFilters": [
            [
              {}
            ]
          ],
          "capacityFilters": [
            [
              {}
            ]
          ],
          "endFilters": [
            [
              {}
            ]
          ],
          "hasTimeOff": true,
          "overtimeFilters": [
            [
              {}
            ]
          ],
          "page": 1,
          "pageSize": 1,
          "sortColumn": "string",
          "startFilters": [
            [
              {}
            ]
          ],
          "workFilters": [
            [
              {}
            ]
          ]
        },
        "billable": true,
        "clients": {
          "contains": "string",
          "ids": [
            [
              "string"
            ]
          ],
          "status": "string"
        },
        "currency": {
          "contains": "string",
          "ids": [
            [
              "string"
            ]
          ],
          "status": "string"
        },
        "customFields": [
          [
            {}
          ]
        ],
        "dateFormat": "string",
        "dateRangeEnd": "string",
        "dateRangeStart": "string",
        "dateRangeType": "string",
        "description": "string",
        "detailedFilter": {
          "auditFilter": {
            "duration": 1,
            "durationShorter": true,
            "withoutProject": true,
            "withoutTask": true
          },
          "options": {
            "totals": "string"
          },
          "page": 1,
          "pageSize": 1,
          "sortColumn": "string"
        },
        "exportType": "string",
        "invoicingState": "string",
        "projects": {
          "contains": "string",
          "ids": [
            [
              "string"
            ]
          ],
          "status": "string"
        },
        "rounding": true,
        "sortOrder": "string",
        "summaryFilter": {
          "groups": [
            [
              "string"
            ]
          ],
          "sortColumn": "string",
          "summaryChartType": "string"
        },
        "tags": {
          "containedInTimeentry": "string",
          "contains": "string",
          "ids": [
            [
              "string"
            ]
          ],
          "status": "string"
        },
        "tasks": {
          "contains": "string",
          "ids": [
            [
              "string"
            ]
          ],
          "status": "string"
        },
        "timeFormat": "string",
        "timeZone": "string",
        "userCustomFields": [
          [
            {}
          ]
        ],
        "userGroups": {
          "contains": "string",
          "ids": [
            [
              "string"
            ]
          ],
          "status": "string"
        },
        "userLocale": "string",
        "users": {
          "contains": "string",
          "ids": [
            [
              "string"
            ]
          ],
          "status": "string"
        },
        "weeklyFilter": {
          "group": "string",
          "subgroup": "string"
        },
        "weekStart": "string",
        "withoutDescription": true,
        "zoomLevel": "string"
      },
      "fixedDate": true,
      "id": "string",
      "isPublic": true,
      "name": "Ava Chen",
      "type": "string",
      "userId": "string",
      "visibleToUserGroups": [
        [
          "string"
        ]
      ],
      "visibleToUsers": [
        [
          "string"
        ]
      ],
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filter` | object |  |
| `filter.amounts[]` | array<string> |  |
| `filter.amountShown` | string |  |
| `filter.approvalState` | string |  |
| `filter.archived` | boolean |  |
| `filter.attendanceFilter` | object |  |
| `filter.attendanceFilter.breakFilters[]` | array<object> |  |
| `filter.attendanceFilter.breakFilters[].filtrationType` | string |  |
| `filter.attendanceFilter.breakFilters[].value` | string |  |
| `filter.attendanceFilter.capacityFilters[]` | array<object> |  |
| `filter.attendanceFilter.capacityFilters[].filtrationType` | string |  |
| `filter.attendanceFilter.capacityFilters[].value` | string |  |
| `filter.attendanceFilter.endFilters[]` | array<object> |  |
| `filter.attendanceFilter.endFilters[].filtrationType` | string |  |
| `filter.attendanceFilter.endFilters[].value` | string |  |
| `filter.attendanceFilter.hasTimeOff` | boolean |  |
| `filter.attendanceFilter.overtimeFilters[]` | array<object> |  |
| `filter.attendanceFilter.overtimeFilters[].filtrationType` | string |  |
| `filter.attendanceFilter.overtimeFilters[].value` | string |  |
| `filter.attendanceFilter.page` | number |  |
| `filter.attendanceFilter.pageSize` | number |  |
| `filter.attendanceFilter.sortColumn` | string |  |
| `filter.attendanceFilter.startFilters[]` | array<object> |  |
| `filter.attendanceFilter.startFilters[].filtrationType` | string |  |
| `filter.attendanceFilter.startFilters[].value` | string |  |
| `filter.attendanceFilter.workFilters[]` | array<object> |  |
| `filter.attendanceFilter.workFilters[].filtrationType` | string |  |
| `filter.attendanceFilter.workFilters[].value` | string |  |
| `filter.billable` | boolean |  |
| `filter.clients` | object |  |
| `filter.clients.contains` | string |  |
| `filter.clients.ids[]` | array<string> |  |
| `filter.clients.status` | string |  |
| `filter.currency` | object |  |
| `filter.currency.contains` | string |  |
| `filter.currency.ids[]` | array<string> |  |
| `filter.currency.status` | string |  |
| `filter.customFields[]` | array<object> |  |
| `filter.customFields[].id` | string |  |
| `filter.customFields[].isEmpty` | boolean |  |
| `filter.customFields[].numberCondition` | string |  |
| `filter.customFields[].type` | string |  |
| `filter.customFields[].value` | object |  |
| `filter.dateFormat` | string |  |
| `filter.dateRangeEnd` | string |  |
| `filter.dateRangeStart` | string |  |
| `filter.dateRangeType` | string |  |
| `filter.description` | string |  |
| `filter.detailedFilter` | object |  |
| `filter.detailedFilter.auditFilter` | object |  |
| `filter.detailedFilter.auditFilter.duration` | number |  |
| `filter.detailedFilter.auditFilter.durationShorter` | boolean |  |
| `filter.detailedFilter.auditFilter.withoutProject` | boolean |  |
| `filter.detailedFilter.auditFilter.withoutTask` | boolean |  |
| `filter.detailedFilter.options` | object |  |
| `filter.detailedFilter.options.totals` | string |  |
| `filter.detailedFilter.page` | number |  |
| `filter.detailedFilter.pageSize` | number |  |
| `filter.detailedFilter.sortColumn` | string |  |
| `filter.exportType` | string |  |
| `filter.invoicingState` | string |  |
| `filter.projects` | object |  |
| `filter.projects.contains` | string |  |
| `filter.projects.ids[]` | array<string> |  |
| `filter.projects.status` | string |  |
| `filter.rounding` | boolean |  |
| `filter.sortOrder` | string |  |
| `filter.summaryFilter` | object |  |
| `filter.summaryFilter.groups[]` | array<string> |  |
| `filter.summaryFilter.sortColumn` | string |  |
| `filter.summaryFilter.summaryChartType` | string |  |
| `filter.tags` | object |  |
| `filter.tags.containedInTimeentry` | string |  |
| `filter.tags.contains` | string |  |
| `filter.tags.ids[]` | array<string> |  |
| `filter.tags.status` | string |  |
| `filter.tasks` | object |  |
| `filter.tasks.contains` | string |  |
| `filter.tasks.ids[]` | array<string> |  |
| `filter.tasks.status` | string |  |
| `filter.timeFormat` | string |  |
| `filter.timeZone` | string |  |
| `filter.userCustomFields[]` | array<object> |  |
| `filter.userCustomFields[].id` | string |  |
| `filter.userCustomFields[].isEmpty` | boolean |  |
| `filter.userCustomFields[].numberCondition` | string |  |
| `filter.userCustomFields[].type` | string |  |
| `filter.userCustomFields[].value` | object |  |
| `filter.userGroups` | object |  |
| `filter.userGroups.contains` | string |  |
| `filter.userGroups.ids[]` | array<string> |  |
| `filter.userGroups.status` | string |  |
| `filter.userLocale` | string |  |
| `filter.users` | object |  |
| `filter.users.contains` | string |  |
| `filter.users.ids[]` | array<string> |  |
| `filter.users.status` | string |  |
| `filter.weeklyFilter` | object |  |
| `filter.weeklyFilter.group` | string |  |
| `filter.weeklyFilter.subgroup` | string |  |
| `filter.weekStart` | string |  |
| `filter.withoutDescription` | boolean |  |
| `filter.zoomLevel` | string |  |
| `fixedDate` | boolean |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `name` | string |  |
| `type` | string |  |
| `userId` | string |  |
| `visibleToUserGroups[]` | array<string> |  |
| `visibleToUsers[]` | array<string> |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/shared-reports` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shared-report.md) for the provider-specific parameters and requirements.

