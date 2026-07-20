# Omnara: Get Checkpoint Download Urls



```
POST https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-checkpoint-download-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-checkpoint-download-urls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-checkpoint-download-urls', {
  method: 'POST',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "checkpointBundleUrl": "https://example.com",
      "error": "string",
      "exists": true,
      "headBundleUrl": "https://example.com",
      "headSha": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkpointBundleUrl` | string |  |
| `error` | string |  |
| `exists` | boolean |  |
| `headBundleUrl` | string |  |
| `headSha` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `POST /api/v1/workspaces/{workspaceId}/sync/checkpoint-download-url` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-checkpoint-download-urls.md) for the provider-specific parameters and requirements.

