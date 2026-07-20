# Appwrite: Get index

Retrieves the index from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-get-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-get-index?connectionId=$CONNECTION_ID&databaseId=string&collectionId=string&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "collectionId": "string",
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-get-index?${params}`, {
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
| `key` | string | yes | Index Key. |

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

Through the native Appwrite API, this operation is `GET /databases/{databaseId}/collections/{collectionId}/indexes/{key}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/databases-get-index.md) for the provider-specific parameters and requirements.

