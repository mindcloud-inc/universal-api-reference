# Appwrite: Update float attribute

Updates the float attribute in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-update-float-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-update-float-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "collectionId": "string",
  "key": "string",
  "required": true,
  "default": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-update-float-attribute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "collectionId": "string",
    "key": "string",
    "required": true,
    "default": 1
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
| `key` | string | yes | Attribute Key. |
| `required` | boolean | yes | Is attribute required? |
| `min` | number | no | Minimum value. |
| `max` | number | no | Maximum value. |
| `default` | number | yes | Default value. Cannot be set when required. |
| `newKey` | string | no | New Attribute Key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$updatedAt": "string",
      "array": true,
      "default": 1,
      "error": "string",
      "key": "string",
      "max": 1,
      "min": 1,
      "required": true,
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
| `$createdAt` | string | Attribute creation date in ISO 8601 format. |
| `$updatedAt` | string | Attribute update date in ISO 8601 format. |
| `array` | boolean | Is attribute an array? |
| `default` | number | Default value for attribute when not provided. Cannot be set when attribute is required. |
| `error` | string | Error message. Displays error generated on failure of creating or deleting an attribute. |
| `key` | string | Attribute Key. |
| `max` | number | Maximum value to enforce for new documents. |
| `min` | number | Minimum value to enforce for new documents. |
| `required` | boolean | Is attribute required? |
| `status` | string | Attribute status. Possible values: `available`, `processing`, `deleting`, `stuck`, or `failed` |
| `type` | string | Attribute type. |

## Native endpoint

Through the native Appwrite API, this operation is `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/float/{key}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/databases-update-float-attribute.md) for the provider-specific parameters and requirements.

