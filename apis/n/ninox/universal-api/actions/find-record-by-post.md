# Ninox: Find Record By POST

Finds a record in Ninox by filters.

```
GET https://connect.mindcloud.co/v1/universal/ninox/latest/actions/find-record-by-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/find-record-by-post?connectionId=$CONNECTION_ID&teamId=YcHTn3ir8XNSp5EXK&dbId=database_id&tableId=table_id&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "YcHTn3ir8XNSp5EXK",
  "dbId": "database_id",
  "tableId": "table_id",
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninox/latest/actions/find-record-by-post?${params}`, {
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
| `tableId` | string | yes | Table ID to search. Example: `table_id`. |
| `style` | string | no | Optional response style. Example: `text`. |
| `dateStyle` | string | no | Optional date formatting style. Example: `iso`. |
| `choiceStyle` | string | no | Optional choice formatting style. Example: `text`. |
| `filters` | object | yes | Filter object used to find one record. Example: `[object Object]`. |

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

Through the native Ninox API, this operation is `POST teams/:teamid/databases/:dbid/tables/:tableid/record` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-record-by-post.md) for the provider-specific parameters and requirements.

