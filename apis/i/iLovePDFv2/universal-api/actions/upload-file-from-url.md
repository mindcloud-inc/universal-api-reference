# iLovePDFv2: Upload File From URL

Uploads a file to an iLovePDFv2 task from a URL.

```
POST https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/upload-file-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDFv2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/upload-file-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "server": "string",
  "task": "string",
  "cloudFile": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/upload-file-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "server": "string",
    "task": "string",
    "cloudFile": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `server` | string | yes | Processing server from Start Task. |
| `task` | string | yes | Task ID from Start Task. |
| `cloudFile` | string | yes | Public URL for the source file to upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "server_filename": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `server_filename` | string |  |

## Native endpoint

Through the native iLovePDFv2 API, this operation is `POST https://:server/v1/upload` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-from-url.md) for the provider-specific parameters and requirements.

