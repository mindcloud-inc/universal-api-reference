# Zoho Sheet: List All Tables

Retrieves tables from a Zoho Sheet workbook.

```
GET https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/list-all-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/list-all-tables?connectionId=$CONNECTION_ID&resourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/list-all-tables?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "method": "string",
      "status": "string",
      "tables": [
        [
          {}
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
| `method` | string |  |
| `status` | string |  |
| `tables[]` | array<object> |  |
| `tables[].endColumn` | number |  |
| `tables[].endRow` | number |  |
| `tables[].startColumn` | number |  |
| `tables[].startRow` | number |  |
| `tables[].tableId` | number |  |
| `tables[].tableName` | string |  |
| `tables[].worksheetId` | string |  |
| `tables[].worksheetName` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-tables.md) for the provider-specific parameters and requirements.

