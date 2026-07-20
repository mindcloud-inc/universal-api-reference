# Appwrite: Create collections

Creates collections in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "collectionId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "collectionId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributes` | string | no | Array of attribute definitions to create. Each attribute should contain: key (string), type (string: string, integer, float, boolean, datetime), size (integer, required for string type), required (boolean, optional), default (mixed, optional), array (boolean, optional), and type-specific options. |
| `databaseId` | string | yes | Database ID. |
| `indexes` | string | no | Array of index definitions to create. Each index should contain: key (string), type (string: key, fulltext, unique, spatial), attributes (array of attribute keys), orders (array of ASC/DESC, optional), and lengths (array of integers, optional). |
| `permissions` | string | no | An array of permissions strings. By default, no user is granted with any permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `collectionId` | string | yes | Unique Id. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | string | yes | Collection name. Max length: 128 chars. |
| `permissions[]` | array<string> | no | An array of permissions strings. By default, no user is granted with any permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `documentSecurity` | boolean | no | Enables configuring permissions for individual documents. A user needs one of document or collection level permissions to access a document. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `enabled` | boolean | no | Is collection enabled? When set to 'disabled', users cannot access the collection but Server SDKs with and API key can still read and write to the collection. No data is lost when this is toggled. |
| `attributes[]` | array<object> | no | Array of attribute definitions to create. Each attribute should contain: key (string), type (string: string, integer, float, boolean, datetime), size (integer, required for string type), required (boolean, optional), default (mixed, optional), array (boolean, optional), and type-specific options. |
| `indexes[]` | array<object> | no | Array of index definitions to create. Each index should contain: key (string), type (string: key, fulltext, unique, spatial), attributes (array of attribute keys), orders (array of ASC/DESC, optional), and lengths (array of integers, optional). |

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

Through the native Appwrite API, this operation is `POST /databases/{databaseId}/collections` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/databases-create-collection.md) for the provider-specific parameters and requirements.

