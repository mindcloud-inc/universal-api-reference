# PiAPI/Toolkit: File Upload API

Uploads a file for PiAPI/Toolkit tasks.

```
POST https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/file-upload-api
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Toolkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/file-upload-api" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "Ava Chen",
  "fileData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/file-upload-api', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileName": "Ava Chen",
    "fileData": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileName` | string | yes | Original filename to associate with the uploaded file. |
| `fileData` | string | yes | Base64-encoded file content expected by PiAPI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native PiAPI/Toolkit API, this operation is `POST https://upload.theapi.app/api/ephemeral_resource` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/file-upload-api.md) for the provider-specific parameters and requirements.

