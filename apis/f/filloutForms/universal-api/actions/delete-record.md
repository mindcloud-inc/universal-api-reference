# Fillout Forms: Delete Record

Deletes a record from Fillout.

```
DELETE https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/delete-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/delete-record?connectionId=$CONNECTION_ID&databaseId=base_abc123&tableId=tbl_abc123&recordId=d4b3c2a3-c46b-46a1-a8ec-81b664bb41cb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "base_abc123",
  "tableId": "tbl_abc123",
  "recordId": "d4b3c2a3-c46b-46a1-a8ec-81b664bb41cb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/delete-record?${params}`, {
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
| `recordId` | string | yes | The UUID of the record to delete. Example: `d4b3c2a3-c46b-46a1-a8ec-81b664bb41cb`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the record was deleted. |

## Native endpoint

Through the native Fillout Forms API, this operation is `DELETE https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-record.md) for the provider-specific parameters and requirements.

