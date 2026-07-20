# Appwrite: Create operations

Creates operations in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbcreate-operations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbcreate-operations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbcreate-operations', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `operations` | string | no | Array of staged operations. |
| `transactionId` | string | yes | Transaction ID. |
| `operations[]` | array<object> | no | Array of staged operations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "expiresAt": "string",
      "operations": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Transaction creation time in ISO 8601 format. |
| `$id` | string | Transaction ID. |
| `$updatedAt` | string | Transaction update date in ISO 8601 format. |
| `expiresAt` | string | Expiration time in ISO 8601 format. |
| `operations` | number | Number of operations in the transaction. |
| `status` | string | Current status of the transaction. One of: pending, committing, committed, rolled_back, failed. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /tablesdb/transactions/{transactionId}/operations` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbcreate-operations.md) for the provider-specific parameters and requirements.

