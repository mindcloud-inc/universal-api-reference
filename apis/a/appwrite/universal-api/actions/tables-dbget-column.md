# Appwrite: Get column

Retrieves the column from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-column?connectionId=$CONNECTION_ID&databaseId=string&tableId=string&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "tableId": "string",
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-column?${params}`, {
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
| `tableId` | string | yes | Table ID. |
| `key` | string | yes | Column Key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$updatedAt": "string",
      "array": true,
      "default": true,
      "error": "string",
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
| `default` | boolean | Default value for column when not provided. Cannot be set when column is required. |
| `error` | string | Error message. Displays error generated on failure of creating or deleting an column. |
| `key` | string | Column Key. |
| `required` | boolean | Is column required? |
| `status` | string | Column status. Possible values: `available`, `processing`, `deleting`, `stuck`, or `failed` |
| `type` | string | Column type. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /tablesdb/{databaseId}/tables/{tableId}/columns/{key}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbget-column.md) for the provider-specific parameters and requirements.

