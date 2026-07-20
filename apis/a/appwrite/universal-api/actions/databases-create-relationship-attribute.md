# Appwrite: Create relationship attribute

Creates a new relationship attribute in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-create-relationship-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-create-relationship-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "collectionId": "string",
  "relatedCollectionId": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-create-relationship-attribute', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "collectionId": "string",
    "relatedCollectionId": "string",
    "type": "string"
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
| `relatedCollectionId` | string | yes | Related Collection ID. |
| `type` | string | yes | Relation type |
| `twoWay` | boolean | no | Is Two Way? |
| `key` | string | no | Attribute Key. |
| `twoWayKey` | string | no | Two Way Attribute Key. |
| `onDelete` | string | no | Constraints option |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$updatedAt": "string",
      "array": true,
      "error": "string",
      "key": "string",
      "onDelete": "string",
      "relatedCollection": "string",
      "relationType": "string",
      "required": true,
      "side": "string",
      "status": "string",
      "twoWay": true,
      "twoWayKey": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Attribute creation date in ISO 8601 format. |
| `$updatedAt` | string | Attribute update date in ISO 8601 format. |
| `array` | boolean | Is attribute an array? |
| `error` | string | Error message. Displays error generated on failure of creating or deleting an attribute. |
| `key` | string | Attribute Key. |
| `onDelete` | string | How deleting the parent document will propagate to child documents. |
| `relatedCollection` | string | The ID of the related collection. |
| `relationType` | string | The type of the relationship. |
| `required` | boolean | Is attribute required? |
| `side` | string | Whether this is the parent or child side of the relationship |
| `status` | string | Attribute status. Possible values: `available`, `processing`, `deleting`, `stuck`, or `failed` |
| `twoWay` | boolean | Is the relationship two-way? |
| `twoWayKey` | string | The key of the two-way relationship. |
| `type` | string | Attribute type. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /databases/{databaseId}/collections/{collectionId}/attributes/relationship` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/databases-create-relationship-attribute.md) for the provider-specific parameters and requirements.

