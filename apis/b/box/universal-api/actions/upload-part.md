# Box: Upload Part



```
PUT https://connect.mindcloud.co/v1/universal/box/latest/actions/upload-part
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Box `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/box/latest/actions/upload-part" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "578EAA0B34295198B0E32B085769932C",
  "partStart": "0",
  "partEnd": "8388607",
  "totalFileSize": "32000000",
  "file": "SGVsbG8="
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/box/latest/actions/upload-part', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "578EAA0B34295198B0E32B085769932C",
    "partStart": "0",
    "partEnd": "8388607",
    "totalFileSize": "32000000",
    "file": "SGVsbG8="
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | Upload session ID returned by Create Upload Session. Example: `578EAA0B34295198B0E32B085769932C`. |
| `partStart` | number | yes | Zero-based byte offset where this part starts. Example: `0`. |
| `partEnd` | number | yes | Inclusive byte offset where this part ends. Example: `8388607`. |
| `totalFileSize` | number | yes | Total size of the complete file in bytes. Example: `32000000`. |
| `file` | file | yes | Raw base64 content for this part. It is decoded and sent as the naked request body. Example: `SGVsbG8=`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "part": {
        "offset": 1,
        "partId": "string",
        "sha1": "string",
        "sha512": "string",
        "size": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `part.offset` | number |  |
| `part.partId` | string |  |
| `part.sha1` | string |  |
| `part.sha512` | string |  |
| `part.size` | number |  |

## Native endpoint

Through the native Box API, this operation is `PUT https://upload.box.com/api/2.0/files/upload_sessions/:session_id`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-part.md) for the provider-specific parameters and requirements.

