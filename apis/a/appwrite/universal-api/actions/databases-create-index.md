# Appwrite: Create index

Creates a new index in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-create-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-create-index" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "collectionId": "string",
  "key": "string",
  "type": "string",
  "attributes[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-create-index', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "collectionId": "string",
    "key": "string",
    "type": "string",
    "attributes[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributes` | string | no | Array of attributes to index. Maximum of 100 attributes are allowed, each 32 characters long. |
| `databaseId` | string | yes | Database ID. |
| `lengths` | string | no | Length of index. Maximum of 100 |
| `orders` | string | no | Array of index orders. Maximum of 100 orders are allowed. |
| `collectionId` | string | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). |
| `key` | string | yes | Index Key. |
| `type` | string | yes | Index type. |
| `attributes[]` | array<string> | yes | Array of attributes to index. Maximum of 100 attributes are allowed, each 32 characters long. |
| `orders[]` | array<string> | no | Array of index orders. Maximum of 100 orders are allowed. |
| `lengths[]` | array<number> | no | Length of index. Maximum of 100 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "attributes": [
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
| `attributes` | array<string> | Index attributes. |
| `error` | string | Error message. Displays error generated on failure of creating or deleting an index. |
| `key` | string | Index key. |
| `lengths` | array<number> | Index attributes length. |
| `orders` | array<string> | Index orders. |
| `status` | string | Index status. Possible values: `available`, `processing`, `deleting`, `stuck`, or `failed` |
| `type` | string | Index type. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /databases/{databaseId}/collections/{collectionId}/indexes` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/databases-create-index.md) for the provider-specific parameters and requirements.

