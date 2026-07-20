# iLoveSign: Upload File From URL



```
POST https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/upload-file-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLoveSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/upload-file-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "server": "api11.ilovepdf.com",
  "task": "string",
  "cloudFile": "https://example.com/document.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/upload-file-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "server": "api11.ilovepdf.com",
    "task": "string",
    "cloudFile": "https://example.com/document.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `server` | string | yes | Task-assigned server host returned by Start Sign Task, for example api11.ilovepdf.com. Example: `api11.ilovepdf.com`. |
| `task` | string | yes | Sign task ID returned by Start Sign Task. |
| `cloudFile` | string | yes | Public URL of the PDF file to upload to the sign task. Example: `https://example.com/document.pdf`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native iLoveSign API returns.

## Native endpoint

Through the native iLoveSign API, this operation is `POST https://:server/v1/upload` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-from-url.md) for the provider-specific parameters and requirements.

