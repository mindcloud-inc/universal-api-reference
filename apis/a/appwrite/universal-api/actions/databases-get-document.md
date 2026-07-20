# Appwrite: Get document

Retrieves the document from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-get-document?connectionId=$CONNECTION_ID&databaseId=string&collectionId=string&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "collectionId": "string",
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-get-document?${params}`, {
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
| `collectionId` | string | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). |
| `documentId` | string | yes | Document ID. |
| `queries[]` | array<string> | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. Accepts multiple values as an array. |
| `transactionId` | string | no | Transaction ID to read uncommitted changes within the transaction. |

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

Through the native Appwrite API, this operation is `GET /databases/{databaseId}/collections/{collectionId}/documents/{documentId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/databases-get-document.md) for the provider-specific parameters and requirements.

