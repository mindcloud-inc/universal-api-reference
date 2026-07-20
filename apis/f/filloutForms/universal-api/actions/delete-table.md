# Fillout Forms: Delete Table

Deletes a table from Fillout.

```
DELETE https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/delete-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/delete-table?connectionId=$CONNECTION_ID&databaseId=67ef4d500c50cce9&tableId=t7nUTgYUjzF" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "67ef4d500c50cce9",
  "tableId": "t7nUTgYUjzF"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/delete-table?${params}`, {
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
| `databaseId` | string | yes | The unique identifier of the database Example: `67ef4d500c50cce9`. |
| `tableId` | string | yes | The unique identifier of the table. You can also use the table name instead of the ID. Example: `t7nUTgYUjzF`. |

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
| `deleted` | boolean | Whether the table was deleted. |

## Native endpoint

Through the native Fillout Forms API, this operation is `DELETE https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-table.md) for the provider-specific parameters and requirements.

