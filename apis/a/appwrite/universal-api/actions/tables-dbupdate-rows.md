# Appwrite: Update rows

Updates the rows in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbupdate-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbupdate-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "tableId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbupdate-rows', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "tableId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | Database ID. |
| `queries` | string | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. |
| `tableId` | string | yes | Table ID. |
| `data` | object | no | Row data as JSON object. Include only column and value pairs to be updated. |
| `queries[]` | array<string> | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. |
| `transactionId` | string | no | Transaction ID for staging the operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rows": [
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
| `rows` | array<object> | List of rows. |
| `total` | number | Total number of rows that matched your query. |

## Native endpoint

Through the native Appwrite API, this operation is `PATCH /tablesdb/{databaseId}/tables/{tableId}/rows` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbupdate-rows.md) for the provider-specific parameters and requirements.

