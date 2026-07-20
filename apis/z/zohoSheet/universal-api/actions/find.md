# Zoho Sheet: Find

Finds matching content in Zoho Sheet.

```
GET https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/find
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/find?connectionId=$CONNECTION_ID&resourceId=string&search=string&scope=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string",
  "search": "string",
  "scope": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/find?${params}`, {
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
| `resourceId` | string | yes | The workbook resource ID. |
| `search` | string | yes | The string that needs to be searched |
| `scope` | string | yes | workbook \| worksheet \| row \| column |
| `worksheetName` | string | no | Name of the worksheet if scope is either worksheet, or row, or column |
| `row` | number | no | Required if the scope is row |
| `column` | number | no | Required if the scope is column |
| `isCaseSensitive` | boolean | no | If set to true upper case and lower case characters will be different during search. By default it is false |
| `isExactMatch` | boolean | no | If set to true the search will match with the full content of the cell. |

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
| `cells[].columnIndex` | number |  |
| `cells[].content` | string |  |
| `cells[].rowIndex` | number |  |
| `cells[].worksheetId` | string |  |
| `cells[].worksheetName` | string |  |
| `matchesFound` | number |  |
| `method` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find.md) for the provider-specific parameters and requirements.

