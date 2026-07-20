# Microsoft 365 Excel: List Table Rows

Retrieves rows from a Microsoft 365 Excel table.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/list-table-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/list-table-rows?connectionId=$CONNECTION_ID&driveItemId=string&tableName=Table1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driveItemId": "string",
  "tableName": "Table1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/list-table-rows?${params}`, {
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
| `tableName` | string | yes | Example: `Table1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "index": 1,
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
| `index` | number |  |
| `values` | array<object> |  |

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/tables('{{tableName}}')/rows` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-table-rows.md) for the provider-specific parameters and requirements.

