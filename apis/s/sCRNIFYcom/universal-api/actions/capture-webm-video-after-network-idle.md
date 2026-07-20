# SCRNIFY.com: Capture WEBM Video After Network Idle

Captures a WEBM video with SCRNIFY.com after network idle.

```
GET https://connect.mindcloud.co/v1/universal/sCRNIFYcom/latest/actions/capture-webm-video-after-network-idle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SCRNIFY.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sCRNIFYcom/latest/actions/capture-webm-video-after-network-idle?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sCRNIFYcom/latest/actions/capture-webm-video-after-network-idle?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | URL of the page to capture. Example: `https://example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SCRNIFY.com API returns.

## Native endpoint

Through the native SCRNIFY.com API, this operation is `GET /capture` (base URL `https://api.scrnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capture-webm-video-after-network-idle.md) for the provider-specific parameters and requirements.

