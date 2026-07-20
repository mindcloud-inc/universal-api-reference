# Smartsheet: Sort Sheet Rows

Sorts rows in a Smartsheet sheet.

```
PUT https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/sort-sheet-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/sort-sheet-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sheetId": 1,
  "sortCriteria[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/sort-sheet-rows', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sheetId": 1,
    "sortCriteria[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sheetId` | number | yes |  |
| `sortCriteria[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": "string",
      "cellImageUploadEnabled": true,
      "columns": [
        {
          "id": 1,
          "index": 1,
          "primary": true,
          "title": "string",
          "type": "string",
          "validation": true,
          "version": 1,
          "width": 1
        }
      ],
      "createdAt": "string",
      "dependenciesEnabled": true,
      "effectiveAttachmentOptions": [
        "string"
      ],
      "ganttEnabled": true,
      "hasSummaryFields": true,
      "id": 1,
      "isMultiPicklistEnabled": true,
      "modifiedAt": "string",
      "name": "Ava Chen",
      "permalink": "https://example.com",
      "resourceManagementEnabled": true,
      "resourceManagementType": "string",
      "rows": [
        {
          "cells": [
            {
              "columnId": 1,
              "displayValue": "string",
              "value": "string"
            }
          ],
          "createdAt": "string",
          "expanded": true,
          "id": 1,
          "modifiedAt": "string",
          "rowNumber": 1
        }
      ],
      "totalRowCount": 1,
      "userPermissions": {
        "summaryPermissions": "string"
      },
      "userSettings": {
        "criticalPathEnabled": true,
        "displaySummaryTasks": true
      },
      "version": 1,
      "workspace": {
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string |  |
| `cellImageUploadEnabled` | boolean |  |
| `columns[].id` | number |  |
| `columns[].index` | number |  |
| `columns[].primary` | boolean |  |
| `columns[].title` | string |  |
| `columns[].type` | string |  |
| `columns[].validation` | boolean |  |
| `columns[].version` | number |  |
| `columns[].width` | number |  |
| `createdAt` | string |  |
| `dependenciesEnabled` | boolean |  |
| `effectiveAttachmentOptions[]` | string |  |
| `ganttEnabled` | boolean |  |
| `hasSummaryFields` | boolean |  |
| `id` | number |  |
| `isMultiPicklistEnabled` | boolean |  |
| `modifiedAt` | string |  |
| `name` | string |  |
| `permalink` | string |  |
| `resourceManagementEnabled` | boolean |  |
| `resourceManagementType` | string |  |
| `rows[].cells[].columnId` | number |  |
| `rows[].cells[].displayValue` | string |  |
| `rows[].cells[].value` | string |  |
| `rows[].createdAt` | string |  |
| `rows[].expanded` | boolean |  |
| `rows[].id` | number |  |
| `rows[].modifiedAt` | string |  |
| `rows[].rowNumber` | number |  |
| `totalRowCount` | number |  |
| `userPermissions.summaryPermissions` | string |  |
| `userSettings.criticalPathEnabled` | boolean |  |
| `userSettings.displaySummaryTasks` | boolean |  |
| `version` | number |  |
| `workspace.id` | number |  |
| `workspace.name` | string |  |

## Native endpoint

Through the native Smartsheet API, this operation is `POST /sheets/:sheetId/sort` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sort-sheet-rows.md) for the provider-specific parameters and requirements.

