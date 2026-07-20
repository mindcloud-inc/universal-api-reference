# Zoho Sheet: Find and Replace

Finds and replaces matching content in Zoho Sheet.

```
PUT https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/find-and-replace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/find-and-replace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "string",
  "search": "string",
  "replaceWith": "string",
  "scope": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/find-and-replace', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "string",
    "search": "string",
    "replaceWith": "string",
    "scope": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | string | yes | The workbook resource ID. |
| `search` | string | yes | The string that needs to be replaced |
| `replaceWith` | string | yes | New replaced string |
| `scope` | string | yes | workbook \| worksheet \| row \| column |
| `worksheetName` | string | no | Required if the scope is either worksheet, or row, or column |
| `row` | number | no | Required if the scope is row |
| `column` | number | no | Required if the scope is column |
| `isCaseSensitive` | boolean | no | If set to true upper case and lower case characters will be different during search. By default it is false |
| `isExactMatch` | boolean | no | If set to true the search with will match with the full content of the cell. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `worksheetId` | string | no | Alternatively worksheet_id can be used instead of worksheet_name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cells": [
        [
          {}
        ]
      ],
      "matchesFound": 1,
      "method": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cells[]` | array<object> |  |
| `cells[].cellValue` | string |  |
| `cells[].columnIndex` | number |  |
| `cells[].formula` | string |  |
| `cells[].rowIndex` | number |  |
| `cells[].sheetName` | string |  |
| `cells[].worksheetId` | string |  |
| `matchesFound` | number |  |
| `method` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-and-replace.md) for the provider-specific parameters and requirements.

