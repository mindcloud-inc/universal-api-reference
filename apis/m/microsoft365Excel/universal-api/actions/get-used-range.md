# Microsoft 365 Excel: Get Used Range

Retrieves the used range from a Microsoft 365 Excel worksheet.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/get-used-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/get-used-range?connectionId=$CONNECTION_ID&driveItemId=string&worksheetName=RuntimeVerify" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driveItemId": "string",
  "worksheetName": "RuntimeVerify"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/get-used-range?${params}`, {
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
| `driveItemId` | string | yes |  |
| `worksheetName` | string | yes | Example: `RuntimeVerify`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "addressLocal": "string",
      "columnCount": 1,
      "rowCount": 1,
      "values": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `addressLocal` | string |  |
| `columnCount` | number |  |
| `rowCount` | number |  |
| `values` | array<object> |  |

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/usedRange` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-used-range.md) for the provider-specific parameters and requirements.

