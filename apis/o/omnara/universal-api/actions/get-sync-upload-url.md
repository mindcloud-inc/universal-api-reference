# Omnara: Get Sync Upload Url



```
POST https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-sync-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-sync-upload-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-sync-upload-url', {
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
      "expiresAt": "string",
      "storageKey": "string",
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | string |  |
| `storageKey` | string |  |
| `uploadUrl` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `POST /api/v1/workspaces/{workspaceId}/sync/upload-url` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sync-upload-url.md) for the provider-specific parameters and requirements.

