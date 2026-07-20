# Clockify: Update Shared Report

Updates an existing shared report in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-shared-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-shared-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-shared-report', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen",
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fixedDate` | boolean | no |  |
| `id` | string | yes |  |
| `isPublic` | boolean | no |  |
| `name` | string | yes |  |
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

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/shared-reports/:id` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shared-report.md) for the provider-specific parameters and requirements.

