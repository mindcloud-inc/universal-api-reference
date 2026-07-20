# Appwrite: Get transaction

Retrieves transaction details from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-transaction?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-transaction?${params}`, {
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
| `transactionId` | string | yes | Transaction ID. |

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

Through the native Appwrite API, this operation is `GET /tablesdb/transactions/{transactionId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbget-transaction.md) for the provider-specific parameters and requirements.

