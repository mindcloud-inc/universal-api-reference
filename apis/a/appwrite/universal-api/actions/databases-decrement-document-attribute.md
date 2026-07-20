# Appwrite: Decrement document attribute

Decrements the document attribute in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-decrement-document-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-decrement-document-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "collectionId": "string",
  "documentId": "string",
  "attribute": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-decrement-document-attribute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "collectionId": "string",
    "documentId": "string",
    "attribute": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | Database ID. |
| `collectionId` | string | yes | Collection ID. |
| `documentId` | string | yes | Document ID. |
| `attribute` | string | yes | Attribute key. |
| `value` | number | no | Value to increment the attribute by. The value must be a number. |
| `min` | number | no | Minimum value for the attribute. If the current value is lesser than this value, an exception will be thrown. |
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

Through the native Appwrite API, this operation is `PATCH /databases/{databaseId}/collections/{collectionId}/documents/{documentId}/{attribute}/decrement` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/databases-decrement-document-attribute.md) for the provider-specific parameters and requirements.

