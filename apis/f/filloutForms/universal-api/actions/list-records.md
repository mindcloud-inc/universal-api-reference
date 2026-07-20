# Fillout Forms: List Records

Retrieves records from a Fillout table.

```
GET https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-records?connectionId=$CONNECTION_ID&databaseId=base_abc123&tableId=tbl_abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "base_abc123",
  "tableId": "tbl_abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-records?${params}`, {
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
| `databaseId` | string | yes | The unique identifier of the database. Example: `base_abc123`. |
| `tableId` | string | yes | The unique identifier of the table. You can also use the table name instead of the ID. Example: `tbl_abc123`. |
| `limit` | number | no | Number of records to return. Default is 500 and the maximum is 2000. Example: `100`. |
| `offset` | number | no | Number of records to skip for pagination. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "records": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean | Whether more records are available. |
| `records` | array<object> | Records returned for the query. |
| `total` | number | Total matching records. |

## Native endpoint

Through the native Fillout Forms API, this operation is `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/list` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.

