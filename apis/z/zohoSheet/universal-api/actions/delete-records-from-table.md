# Zoho Sheet: Delete Records from Table

Deletes records from a table in Zoho Sheet.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/delete-records-from-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/delete-records-from-table?connectionId=$CONNECTION_ID&resourceId=string&tableName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string",
  "tableName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/delete-records-from-table?${params}`, {
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
| `tableName` | string | yes | Name of the table whose records needs to be deleted |
| `criteriaJson` | string | no | Optional parameter. Can be used to filter records. Provide this value as a valid JSON string. |
| `criteriaPattern` | string | no | Required when more than 1 criteria is available under criteria_json |
| `firstMatchOnly` | boolean | no | Optional parameter. If true and if there are multiple records on the specified criteria, records will be updated for first match alone. Otherwise, all the matched records will be updated. |
| `isCaseSensitive` | boolean | no | Optional parameter. By default it is true. Can be set as false for case insensitive search. |

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
      "noOfRowsDeleted": 1,
      "noOfRowsRemaining": 1,
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
| `noOfRowsDeleted` | number |  |
| `noOfRowsRemaining` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records-from-table.md) for the provider-specific parameters and requirements.

