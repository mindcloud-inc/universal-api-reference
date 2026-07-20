# Ninox: Delete Records

Deletes multiple records from a Ninox table.

```
DELETE https://connect.mindcloud.co/v1/universal/ninox/latest/actions/delete-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/delete-records?connectionId=$CONNECTION_ID&teamId=YcHTn3ir8XNSp5EXK&dbId=database_id&tableId=table_id&recordIds=1%2C2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "YcHTn3ir8XNSp5EXK",
  "dbId": "database_id",
  "tableId": "table_id",
  "recordIds": "1,2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninox/latest/actions/delete-records?${params}`, {
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
| `teamId` | string | yes | Workspace ID that owns the database. Example: `YcHTn3ir8XNSp5EXK`. |
| `dbId` | string | yes | Database ID that owns the table. Example: `database_id`. |
| `tableId` | string | yes | Table ID to delete records from. Example: `table_id`. |
| `recordIds` | list<number> | yes | Array of record IDs to delete. Example: `1,2`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ninox API returns.

## Native endpoint

Through the native Ninox API, this operation is `DELETE teams/:teamid/databases/:dbid/tables/:tableid/records` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records.md) for the provider-specific parameters and requirements.

