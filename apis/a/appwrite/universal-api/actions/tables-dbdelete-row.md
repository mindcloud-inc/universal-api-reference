# Appwrite: Delete row

Deletes the row from your Appwrite project.

```
DELETE https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbdelete-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbdelete-row?connectionId=$CONNECTION_ID&databaseId=string&tableId=string&rowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "tableId": "string",
  "rowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbdelete-row?${params}`, {
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
| `transactionId` | string | no | Transaction ID for staging the operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when the request succeeds. |

## Native endpoint

Through the native Appwrite API, this operation is `DELETE /tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbdelete-row.md) for the provider-specific parameters and requirements.

