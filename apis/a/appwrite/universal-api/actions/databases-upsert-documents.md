# Appwrite: Upsert documents

Upserts documents in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-upsert-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-upsert-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "collectionId": "string",
  "documents[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-upsert-documents', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "collectionId": "string",
    "documents[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | Database ID. |
| `documents` | string | no | Array of document data as JSON objects. May contain partial documents. |
| `collectionId` | string | yes | Collection ID. |
| `documents[]` | array<object> | yes | Array of document data as JSON objects. May contain partial documents. |
| `transactionId` | string | no | Transaction ID for staging the operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
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
| `documents` | array<object> | List of documents. |
| `total` | number | Total number of documents that matched your query. |

## Native endpoint

Through the native Appwrite API, this operation is `PUT /databases/{databaseId}/collections/{collectionId}/documents` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/databases-upsert-documents.md) for the provider-specific parameters and requirements.

