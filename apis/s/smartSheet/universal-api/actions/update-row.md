# Smartsheet: Update Row

Updates a row in a Smartsheet sheet.

```
PUT https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/update-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/update-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sheetId": 1,
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/update-row', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sheetId": 1,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sheetId` | number | yes |  |
| `id` | number | yes |  |
| `cells[]` | array<object> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parentId` | number | no |  |
| `siblingId` | number | no |  |
| `above` | boolean | no |  |
| `allowPartialSuccess` | boolean | no |  |
| `overrideValidation` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": [
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
          "locked": true,
          "lockedForUser": true,
          "modifiedAt": "string",
          "rowNumber": 1
        }
      ],
      "resultCode": 1,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `result[].cells[].columnId` | number |  |
| `result[].cells[].displayValue` | string |  |
| `result[].cells[].value` | string |  |
| `result[].createdAt` | string |  |
| `result[].expanded` | boolean |  |
| `result[].id` | number |  |
| `result[].locked` | boolean |  |
| `result[].lockedForUser` | boolean |  |
| `result[].modifiedAt` | string |  |
| `result[].rowNumber` | number |  |
| `resultCode` | number |  |
| `version` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `PUT /sheets/:sheetId/rows` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-row.md) for the provider-specific parameters and requirements.

