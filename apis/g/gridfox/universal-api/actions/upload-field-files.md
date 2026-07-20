# Gridfox: Upload Field Files

Adds files to a file field in Gridfox.

```
PUT https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/upload-field-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridfox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/upload-field-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/upload-field-files', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldName` | string | no | Gridfox file field name from the path parameter. |
| `referenceFieldValue` | string | no | Record reference field value from the path parameter. |
| `tableName` | string | no | Gridfox table name from the path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the file upload succeeded. |

## Native endpoint

Through the native Gridfox API, this operation is `POST /data/:tableName/:referenceFieldValue/:fieldName` (base URL `https://api.gridfox.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-field-files.md) for the provider-specific parameters and requirements.

