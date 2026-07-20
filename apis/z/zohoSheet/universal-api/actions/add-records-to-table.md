# Zoho Sheet: Add Records to Table

Adds records to a table in Zoho Sheet.

```
POST https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/add-records-to-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/add-records-to-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "string",
  "tableName": "Ava Chen",
  "jsonData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/add-records-to-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "string",
    "tableName": "Ava Chen",
    "jsonData": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | string | yes | The workbook resource ID. |
| `tableName` | string | yes | Name of the table |
| `insertAtTop` | boolean | no | Optional parameter. Can be set as true to add records at the top. By default it is false. |
| `jsonData` | string | yes | JSON Array. Example : [{"Name":"Joe","Region":"South","Units":284},{"Name":"Beth","Region":"East","Units":290}]. "Name", "Region", and "Units" are the table headers. Provide this value as a valid JSON string. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | no | Alternatively table_id can be used instead of table_name |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `method` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-records-to-table.md) for the provider-specific parameters and requirements.

