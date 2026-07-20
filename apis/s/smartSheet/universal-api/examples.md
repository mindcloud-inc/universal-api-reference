# Smartsheet Universal API Examples

These examples use the MindCloud API key and Smartsheet connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Row

Retrieves a row from a Smartsheet sheet.

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

Example response:

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

See the full [Get Row action reference](actions/get-row.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartSheet/latest/actions/get-row).

## Copy Rows

Copies rows to another sheet in Smartsheet.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/copy-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sheetId": 1,
  "rowIds[]": [
    1
  ],
  "to": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/copy-rows', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sheetId": 1,
    "rowIds[]": [1],
    "to": {}
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "destinationSheetId": 1,
      "rowMappings": [
        {
          "from": 1,
          "to": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Copy Rows action reference](actions/copy-rows.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartSheet/latest/actions/copy-rows).
