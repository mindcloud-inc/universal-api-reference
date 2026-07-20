# Microsoft 365: Get Worksheet Used Range

Retrieves a worksheet's used range from Microsoft 365.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-worksheet-used-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-worksheet-used-range?connectionId=$CONNECTION_ID&driveItemId=01QQGNZQWRVBAJPBCNI5E2QBRQJ7UFXKNO&worksheetName=Emails_Raw" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driveItemId": "01QQGNZQWRVBAJPBCNI5E2QBRQJ7UFXKNO",
  "worksheetName": "Emails_Raw"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-worksheet-used-range?${params}`, {
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
| `driveItemId` | string | yes | Microsoft Graph drive item ID for the Excel workbook. Example: `01QQGNZQWRVBAJPBCNI5E2QBRQJ7UFXKNO`. |
| `worksheetName` | string | yes | Name of the worksheet to read. Example: `Emails_Raw`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "cellCount": 1,
      "columnCount": 1,
      "columnIndex": 1,
      "rowCount": 1,
      "rowIndex": 1,
      "text": [
        [
          "string"
        ]
      ],
      "values": [
        [
          "string"
        ]
      ],
      "valueTypes": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Workbook address of the used range. |
| `cellCount` | number | Number of cells in the used range. |
| `columnCount` | number | Number of columns in the used range. |
| `columnIndex` | number | Zero-based column index where the used range begins. |
| `rowCount` | number | Number of rows in the used range. |
| `rowIndex` | number | Zero-based row index where the used range begins. |
| `text` | array<array> | Two-dimensional array of formatted cell text. |
| `values` | array<array> | Two-dimensional array of cell values from the used range. |
| `valueTypes` | array<array> | Two-dimensional array of value types for cells in the used range. |

## Native endpoint

Through the native Microsoft 365 API, this operation is `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/usedRange()` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-worksheet-used-range.md) for the provider-specific parameters and requirements.

