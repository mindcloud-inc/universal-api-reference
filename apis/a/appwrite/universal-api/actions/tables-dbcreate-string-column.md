# Appwrite: Create string column

Creates a new string column in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbcreate-string-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbcreate-string-column" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "tableId": "string",
  "key": "string",
  "size": 1,
  "required": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbcreate-string-column', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "tableId": "string",
    "key": "string",
    "size": 1,
    "required": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | Database ID. |
| `tableId` | string | yes | Table ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/references/cloud/server-dart/tablesDB#createTable). |
| `key` | string | yes | Column Key. |
| `size` | number | yes | Column size for text columns, in number of characters. |
| `required` | boolean | yes | Is column required? |
| `default` | string | no | Default value for column when not provided. Cannot be set when column is required. |
| `array` | boolean | no | Is column an array? |
| `encrypt` | boolean | no | Toggle encryption for the column. Encryption enhances security by not storing any plain text values in the database. However, encrypted columns cannot be queried. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$updatedAt": "string",
      "array": true,
      "default": "string",
      "encrypt": true,
      "error": "string",
      "key": "string",
      "required": true,
      "size": 1,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Column creation date in ISO 8601 format. |
| `$updatedAt` | string | Column update date in ISO 8601 format. |
| `array` | boolean | Is column an array? |
| `default` | string | Default value for column when not provided. Cannot be set when column is required. |
| `encrypt` | boolean | Defines whether this column is encrypted or not. |
| `error` | string | Error message. Displays error generated on failure of creating or deleting an column. |
| `key` | string | Column Key. |
| `required` | boolean | Is column required? |
| `size` | number | Column size. |
| `status` | string | Column status. Possible values: `available`, `processing`, `deleting`, `stuck`, or `failed` |
| `type` | string | Column type. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /tablesdb/{databaseId}/tables/{tableId}/columns/string` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbcreate-string-column.md) for the provider-specific parameters and requirements.

