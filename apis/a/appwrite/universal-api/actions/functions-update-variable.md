# Appwrite: Update variable

Updates the variable in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-update-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-update-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "functionId": "string",
  "variableId": "string",
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-update-variable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "functionId": "string",
    "variableId": "string",
    "key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `functionId` | string | yes | Function unique ID. |
| `variableId` | string | yes | Variable unique ID. |
| `key` | string | yes | Variable key. Max length: 255 chars. |
| `value` | string | no | Variable value. Max length: 8192 chars. |
| `secret` | boolean | no | Secret variables can be updated or deleted, but only functions can read them during build and runtime. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "key": "string",
      "resourceId": "string",
      "resourceType": "string",
      "secret": true,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Variable creation date in ISO 8601 format. |
| `$id` | string | Variable ID. |
| `$updatedAt` | string | Variable creation date in ISO 8601 format. |
| `key` | string | Variable key. |
| `resourceId` | string | ID of resource to which the variable belongs. If resourceType is "project", it is empty. If resourceType is "function", it is ID of the function. |
| `resourceType` | string | Service to which the variable belongs. Possible values are "project", "function" |
| `secret` | boolean | Variable secret flag. Secret variables can only be updated or deleted, but never read. |
| `value` | string | Variable value. |

## Native endpoint

Through the native Appwrite API, this operation is `PUT /functions/{functionId}/variables/{variableId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/functions-update-variable.md) for the provider-specific parameters and requirements.

