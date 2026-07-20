# Appwrite: Get index

Retrieves the index from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-index?connectionId=$CONNECTION_ID&databaseId=string&tableId=string&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "tableId": "string",
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-index?${params}`, {
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
| `databaseId` | string | yes | Database ID. |
| `tableId` | string | yes | Table ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/references/cloud/server-dart/tablesDB#createTable). |
| `key` | string | yes | Index Key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "columns": [
        "string"
      ],
      "error": "string",
      "key": "string",
      "lengths": [
        1
      ],
      "orders": [
        "string"
      ],
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
| `$createdAt` | string | Index creation date in ISO 8601 format. |
| `$id` | string | Index ID. |
| `$updatedAt` | string | Index update date in ISO 8601 format. |
| `columns` | array<string> | Index columns. |
| `error` | string | Error message. Displays error generated on failure of creating or deleting an index. |
| `key` | string | Index Key. |
| `lengths` | array<number> | Index columns length. |
| `orders` | array<string> | Index orders. |
| `status` | string | Index status. Possible values: `available`, `processing`, `deleting`, `stuck`, or `failed` |
| `type` | string | Index type. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /tablesdb/{databaseId}/tables/{tableId}/indexes/{key}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbget-index.md) for the provider-specific parameters and requirements.

