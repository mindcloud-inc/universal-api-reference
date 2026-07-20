# Smartsheet: Get Row

Retrieves a row from a Smartsheet sheet.

```
GET https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/get-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/get-row?connectionId=$CONNECTION_ID&sheetId=1&rowId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sheetId": "1",
  "rowId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/get-row?${params}`, {
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
| `sheetId` | number | yes |  |
| `rowId` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no |  |
| `exclude` | string | no |  |
| `level` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": "string",
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
      "rowNumber": 1,
      "sheetId": 1,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string |  |
| `cells[].columnId` | number |  |
| `cells[].displayValue` | string |  |
| `cells[].value` | string |  |
| `createdAt` | string |  |
| `expanded` | boolean |  |
| `id` | number |  |
| `modifiedAt` | string |  |
| `rowNumber` | number |  |
| `sheetId` | number |  |
| `version` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `GET /sheets/:sheetId/rows/:rowId` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-row.md) for the provider-specific parameters and requirements.

