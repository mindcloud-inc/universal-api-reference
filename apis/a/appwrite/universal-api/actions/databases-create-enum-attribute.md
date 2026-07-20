# Appwrite: Create enum attribute

Creates a new enum attribute in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-create-enum-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-create-enum-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "collectionId": "string",
  "key": "string",
  "elements[]": [
    "string"
  ],
  "required": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-create-enum-attribute', {
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
    "elements[]": ["string"],
    "required": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | Database ID. |
| `elements` | string | no | Array of enum values. |
| `collectionId` | string | yes | Collection ID. |
| `key` | string | yes | Attribute Key. |
| `elements[]` | array<string> | yes | Array of enum values. |
| `required` | boolean | yes | Is attribute required? |
| `default` | string | no | Default value for attribute when not provided. Cannot be set when attribute is required. |
| `array` | boolean | no | Is attribute an array? |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$updatedAt": "string",
      "array": true,
      "default": "string",
      "elements": [
        "string"
      ],
      "error": "string",
      "format": "string",
      "key": "string",
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
| `default` | string | Default value for attribute when not provided. Cannot be set when attribute is required. |
| `elements` | array<string> | Array of elements in enumerated type. |
| `error` | string | Error message. Displays error generated on failure of creating or deleting an attribute. |
| `format` | string | String format. |
| `key` | string | Attribute Key. |
| `required` | boolean | Is attribute required? |
| `status` | string | Attribute status. Possible values: `available`, `processing`, `deleting`, `stuck`, or `failed` |
| `type` | string | Attribute type. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /databases/{databaseId}/collections/{collectionId}/attributes/enum` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/databases-create-enum-attribute.md) for the provider-specific parameters and requirements.

