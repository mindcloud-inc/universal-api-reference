# Appwrite: Update document

Updates the document in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "collectionId": "string",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-update-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "collectionId": "string",
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | Database ID. |
| `permissions` | string | no | An array of permissions strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `collectionId` | string | yes | Collection ID. |
| `documentId` | string | yes | Document ID. |
| `data` | object | no | Document data as JSON object. Include only attribute and value pairs to be updated. |
| `permissions[]` | array<string> | no | An array of permissions strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `transactionId` | string | no | Transaction ID for staging the operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$collectionId": "string",
      "$createdAt": "string",
      "$databaseId": "string",
      "$id": "string",
      "$permissions": [
        "string"
      ],
      "$sequence": 1,
      "$updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$collectionId` | string | Collection ID. |
| `$createdAt` | string | Document creation date in ISO 8601 format. |
| `$databaseId` | string | Database ID. |
| `$id` | string | Document ID. |
| `$permissions` | array<string> | Document permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `$sequence` | number | Document automatically incrementing ID. |
| `$updatedAt` | string | Document update date in ISO 8601 format. |

## Native endpoint

Through the native Appwrite API, this operation is `PATCH /databases/{databaseId}/collections/{collectionId}/documents/{documentId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/databases-update-document.md) for the provider-specific parameters and requirements.

