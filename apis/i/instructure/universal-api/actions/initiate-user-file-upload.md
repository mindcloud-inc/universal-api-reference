# Instructure: Initiate User File Upload

Initiates a user file upload in Instructure Canvas.

```
POST https://connect.mindcloud.co/v1/universal/instructure/latest/actions/initiate-user-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/initiate-user-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "size": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/initiate-user-file-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "size": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentType` | string | no | MIME type of the file. |
| `name` | string | yes | Name of the file to upload. |
| `parentFolderId` | string | no | Folder ID to upload into. |
| `size` | number | yes | Size of the file in bytes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "upload_params": {},
      "upload_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `upload_params` | object |  |
| `upload_url` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `POST /users/self/files` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initiate-user-file-upload.md) for the provider-specific parameters and requirements.

