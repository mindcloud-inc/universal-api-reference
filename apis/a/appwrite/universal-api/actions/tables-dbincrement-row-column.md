# Appwrite: Increment row column

Increments the row column in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbincrement-row-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbincrement-row-column" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "tableId": "string",
  "rowId": "string",
  "column": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbincrement-row-column', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "tableId": "string",
    "rowId": "string",
    "column": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | Database ID. |
| `tableId` | string | yes | Table ID. |
| `rowId` | string | yes | Row ID. |
| `column` | string | yes | Column key. |
| `value` | number | no | Value to increment the column by. The value must be a number. |
| `max` | number | no | Maximum value for the column. If the current value is greater than this value, an error will be thrown. |
| `transactionId` | string | no | Transaction ID for staging the operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$databaseId": "string",
      "$id": "string",
      "$permissions": [
        "string"
      ],
      "$sequence": 1,
      "$tableId": "string",
      "$updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Row creation date in ISO 8601 format. |
| `$databaseId` | string | Database ID. |
| `$id` | string | Row ID. |
| `$permissions` | array<string> | Row permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `$sequence` | number | Row automatically incrementing ID. |
| `$tableId` | string | Table ID. |
| `$updatedAt` | string | Row update date in ISO 8601 format. |

## Native endpoint

Through the native Appwrite API, this operation is `PATCH /tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}/{column}/increment` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbincrement-row-column.md) for the provider-specific parameters and requirements.

