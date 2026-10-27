# Box: Upload File Version



```
PUT https://connect.mindcloud.co/v1/universal/box/latest/actions/upload-file-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Box `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/box/latest/actions/upload-file-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "123456789",
  "file": "SG9sYSBCb3ggZGVzZGUgTWluZENsb3VkIQ=="
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/box/latest/actions/upload-file-version', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "123456789",
    "file": "SG9sYSBCb3ggZGVzZGUgTWluZENsb3VkIQ=="
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | The file ID to upload a new version for. Example: `123456789`. |
| `fileName` | string | no | Optional replacement filename for the uploaded new version. Example: `report-v2.pdf`. |
| `file` | file | yes | Paste a plain base64 string, a full data URL, or a public HTTPS file URL. Data URLs are stripped to raw base64 automatically before upload. Example: `SG9sYSBCb3ggZGVzZGUgTWluZENsb3VkIQ==`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Optional comma-separated list of file fields to include in the response. Example: `id,type,name,size,parent`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Box API returns.

## Native endpoint

Through the native Box API, this operation is `POST https://upload.box.com/api/2.0/files/:file_id/content` (base URL `https://api.box.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-version.md) for the provider-specific parameters and requirements.

