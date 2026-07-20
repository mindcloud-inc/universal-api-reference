# Proofy: Upload File by URL



```
POST https://connect.mindcloud.co/v1/universal/proofy/latest/actions/upload-file-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Proofy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proofy/latest/actions/upload-file-by-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_name": "Ava Chen",
  "file_url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proofy/latest/actions/upload-file-by-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_name": "Ava Chen",
    "file_url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_name` | string | yes | Name to assign to the uploaded file task. |
| `file_url` | string | yes | Public URL for the file containing email addresses. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Proofy API returns.

## Native endpoint

Through the native Proofy API, this operation is `POST /verify/file/create` (base URL `https://apis.proofy.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-by-url.md) for the provider-specific parameters and requirements.

