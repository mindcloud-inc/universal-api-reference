# Ninox: List Records

Retrieves records from a Ninox table.

```
GET https://connect.mindcloud.co/v1/universal/ninox/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/list-records?connectionId=$CONNECTION_ID&teamId=YcHTn3ir8XNSp5EXK&dbId=database_id&tableId=table_id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "YcHTn3ir8XNSp5EXK",
  "dbId": "database_id",
  "tableId": "table_id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninox/latest/actions/list-records?${params}`, {
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
| `tableId` | string | yes | Table ID whose records to list. Example: `table_id`. |
| `choiceStyle` | string | no | Optional choice formatting style for returned fields. Example: `text`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "fields": {},
      "id": 1,
      "modifiedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Record creation timestamp. |
| `fields` | object | Record field values. |
| `id` | number | Record ID. |
| `modifiedAt` | number | Record last-modified timestamp. |

## Native endpoint

Through the native Ninox API, this operation is `GET teams/:teamid/databases/:dbid/tables/:tableid/records` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.

