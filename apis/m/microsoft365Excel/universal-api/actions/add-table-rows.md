# Microsoft 365 Excel: Add Table Rows

Adds rows to a Microsoft 365 Excel table.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/add-table-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/add-table-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveItemId": "string",
  "tableName": "Table1",
  "values": "April,42"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/add-table-rows', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveItemId": "string",
    "tableName": "Table1",
    "values": "April,42"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driveItemId` | string | yes |  |
| `tableName` | string | yes | Example: `Table1`. |
| `values` | object | yes | Two-dimensional array of row values. Example: `April,42`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `index` | number | no |  |

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

Through the native Microsoft 365 Excel API, this operation is `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/tables('{{tableName}}')/rows/add` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-table-rows.md) for the provider-specific parameters and requirements.

