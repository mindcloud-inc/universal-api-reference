# Cognito Forms: Upload File



```
POST https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cognito Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "File": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "File": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `File` | string | yes | The file to upload (multipart/form-data). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "id": "string",
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | The file content type. |
| `id` | string | The File ID. |
| `name` | string | The file name. |
| `size` | number | The file size in bytes. |

## Native endpoint

Through the native Cognito Forms API, this operation is `POST /files` (base URL `https://www.cognitoforms.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

