# ZapCap: Upload Video By URL

Uploads a video to ZapCap from a public URL.

```
POST https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/upload-video-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZapCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/upload-video-by-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://cdn.zapcap.ai/templates/a51c5222-47a7-4c37-b052-7b9853d66bf6.mp4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/upload-video-by-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://cdn.zapcap.ai/templates/a51c5222-47a7-4c37-b052-7b9853d66bf6.mp4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public MP4 URL to import into ZapCap. Example: `https://cdn.zapcap.ai/templates/a51c5222-47a7-4c37-b052-7b9853d66bf6.mp4`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ZapCap API returns.

## Native endpoint

Through the native ZapCap API, this operation is `POST /videos/url` (base URL `https://api.zapcap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-video-by-url.md) for the provider-specific parameters and requirements.

