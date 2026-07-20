# Appwrite: Get row

Retrieves the row from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-row?connectionId=$CONNECTION_ID&databaseId=string&tableId=string&rowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "tableId": "string",
  "rowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-row?${params}`, {
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
| `rowId` | string | yes | Row ID. |
| `queries[]` | array<string> | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. Accepts multiple values as an array. |
| `transactionId` | string | no | Transaction ID to read uncommitted changes within the transaction. |

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

Through the native Appwrite API, this operation is `GET /tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbget-row.md) for the provider-specific parameters and requirements.

