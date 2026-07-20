# Files.com: Begin File Upload

Begins a file upload in Files.com.

```
POST https://connect.mindcloud.co/v1/universal/filescom/latest/actions/begin-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/begin-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "string",
  "size": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filescom/latest/actions/begin-file-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "path": "string",
    "size": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | yes | Path of the file to upload, including file name. |
| `size` | number | yes | Total file size in bytes. |
| `mkdirParents` | boolean | no | Create missing parent folders automatically when true. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `part` | number | no | Specific multipart upload part number to begin. |
| `parts` | number | no | Total number of multipart upload parts. |
| `ref` | string | no | Resume token from a previous begin-upload response. |
| `restart` | number | no | Restart the upload sequence from a given part index. |
| `withRename` | boolean | no | Allow Files.com to rename the uploaded file to avoid conflicts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "available_parts": 1,
      "expires": "2026-05-07T12:00:00.000Z",
      "headers": {},
      "http_method": "string",
      "next_partsize": 1,
      "parallel_parts": true,
      "parameters": {},
      "part_number": 1,
      "partsize": 1,
      "ref": "string",
      "retry_parts": true,
      "send": {},
      "upload_uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `available_parts` | number |  |
| `expires` | date |  |
| `headers` | object |  |
| `http_method` | string |  |
| `next_partsize` | number |  |
| `parallel_parts` | boolean |  |
| `parameters` | object |  |
| `part_number` | number |  |
| `partsize` | number |  |
| `ref` | string |  |
| `retry_parts` | boolean |  |
| `send` | object |  |
| `upload_uri` | string |  |

## Native endpoint

Through the native Files.com API, this operation is `POST /file_actions/begin_upload/:path` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/begin-file-upload.md) for the provider-specific parameters and requirements.

