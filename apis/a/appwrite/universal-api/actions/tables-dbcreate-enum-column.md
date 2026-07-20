# Appwrite: Create enum column

Creates a new enum column in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbcreate-enum-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbcreate-enum-column" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "tableId": "string",
  "key": "string",
  "elements[]": [
    "string"
  ],
  "required": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbcreate-enum-column', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "tableId": "string",
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
| `tableId` | string | yes | Table ID. |
| `key` | string | yes | Column Key. |
| `elements[]` | array<string> | yes | Array of enum values. |
| `required` | boolean | yes | Is column required? |
| `default` | string | no | Default value for column when not provided. Cannot be set when column is required. |
| `array` | boolean | no | Is column an array? |

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
| `$createdAt` | string | Column creation date in ISO 8601 format. |
| `$updatedAt` | string | Column update date in ISO 8601 format. |
| `array` | boolean | Is column an array? |
| `default` | string | Default value for column when not provided. Cannot be set when column is required. |
| `elements` | array<string> | Array of elements in enumerated type. |
| `error` | string | Error message. Displays error generated on failure of creating or deleting an column. |
| `format` | string | String format. |
| `key` | string | Column Key. |
| `required` | boolean | Is column required? |
| `status` | string | Column status. Possible values: `available`, `processing`, `deleting`, `stuck`, or `failed` |
| `type` | string | Column type. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /tablesdb/{databaseId}/tables/{tableId}/columns/enum` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbcreate-enum-column.md) for the provider-specific parameters and requirements.

