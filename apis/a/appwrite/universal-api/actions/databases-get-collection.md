# Appwrite: Get collection

Retrieves collection details from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-get-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-get-collection?connectionId=$CONNECTION_ID&databaseId=string&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-get-collection?${params}`, {
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
| `collectionId` | string | yes | Collection ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$permissions": [
        "string"
      ],
      "$updatedAt": "string",
      "attributes": [
        "string"
      ],
      "databaseId": "string",
      "documentSecurity": true,
      "enabled": true,
      "indexes": [
        {}
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Collection creation date in ISO 8601 format. |
| `$id` | string | Collection ID. |
| `$permissions` | array<string> | Collection permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `$updatedAt` | string | Collection update date in ISO 8601 format. |
| `attributes` | array<string> | Collection attributes. |
| `databaseId` | string | Database ID. |
| `documentSecurity` | boolean | Whether document-level permissions are enabled. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `enabled` | boolean | Collection enabled. Can be 'enabled' or 'disabled'. When disabled, the collection is inaccessible to users, but remains accessible to Server SDKs using API keys. |
| `indexes` | array<object> | Collection indexes. |
| `name` | string | Collection name. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /databases/{databaseId}/collections/{collectionId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/databases-get-collection.md) for the provider-specific parameters and requirements.

