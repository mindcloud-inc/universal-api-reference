# Zoho Sheet: Update Records in Table

Updates records in a table in Zoho Sheet.

```
PUT https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/update-records-in-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/update-records-in-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "string",
  "tableName": "Ava Chen",
  "data": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/update-records-in-table', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "string",
    "tableName": "Ava Chen",
    "data": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | string | yes | The workbook resource ID. |
| `tableName` | string | yes | Name of the table whose records needs to be updated |
| `criteriaJson` | string | no | Optional parameter. Can be used to filter records. Provide this value as a valid JSON string. |
| `criteriaPattern` | string | no | Required when more than 1 criteria is available under criteria_json |
| `firstMatchOnly` | boolean | no | Optional parameter. If true and if there are multiple records on the specified criteria, records will be updated for first match alone. Otherwise, all the matched records will be updated. |
| `isCaseSensitive` | boolean | no | Optional parameter. By default it is true. Can be set as false for case insensitive search. |
| `data` | string | yes | The JSON data that needs to be updated. Example:{"Month":"May","Amount":50} Provide this value as a valid JSON string. |

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
      "noOfAffectedRows": 1,
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
| `noOfAffectedRows` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-records-in-table.md) for the provider-specific parameters and requirements.

